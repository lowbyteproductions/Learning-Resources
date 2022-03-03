# USB Terminology Notes

*Note: This is mostly in the context of USB <= 2.0*

- USB is complicated
- It's a stack, from the electrical characteristics at the lowest levels to the software abstractions at the highest levels
- It encompasses everything from the connectors, physical wiring, protocols, and (multiple levels of) software

## Devices, functions, interfaces, and endpoints

### Device

From the USB 2.0 spec:

```
A logical or physical entity that performs a function. The actual entity
described depends on the context of the reference. At the lowest level, device
may refer to a single hardware component, as in a memory device. At a higher
level, it may refer to a collection of hardware components that perform a
particular function, such as a USB interface device. At an even higher level,
device may refer to the function performed by an entity attached to the USB;
for example, a data/FAX modem device. Devices may be physical, electrical,
addressable, and logical.
When used as a non-specific reference, a USB device is either a hub or a
function.
```

### Function

```
A USB device that provides a capability to the host, such as an ISDN
connection, a digital microphone, or speakers.
```

### Interface (in the context of a "descriptor")

- Using the word interface here was a bad choice IMO
- A device can have numerous interfaces, each of which implements it's own functionality indpendently
- For example, a webcam can have both a camera and a microphone interface
  - These can be used and driven separately
- There are *many* standard interfaces (e.g. keyboards, mice, webcams, microphones, etc)
  - Operating systems tend to have generic drivers for these devices, so they often "just work" when you plug them in
  - If a device implements a non-standard interface, that is when it needs a 3rd party driver to work

### Endpoint

- Interfaces can have one or more endpoints
- Endpoints are uniquely addressed with a byte, allowing for a maximum of 256 endpoints per device
  - Endpoints with their MSB set are IN (device to host), and ones with their MSB reset are OUT (host to device)
- An endpoint is basically an single directional I/O port (either IN or OUT)
  - The host can send data to a device
  - The host can ask to recieve data from a device
- Endpoints are intrinsically linked with the type of data transfers that they facilitate
  - Since there are different kinds of transfers, there are corresponding kinds of endpoints (an IN and OUT for each)
    - Control
    - Interrupt
    - Bulk
    - Isochronous
- All USB devices must implement endpoint 0, which is a control endpoint.

## Transfers

- All transfers are initiated by the host in USB
  - Even for event driven devices, it's the host's responsiblity to "ask" for the events at the rate which the device wants to send them

### Control transfers

- Control transfers are used to configure the device
- Every device must have at least one endpoint for control, which is at addres 0x00

### Interrupt transfers

- Confusingly, these are not *really* interrupts in the sense of a CPU or microcontroller
- The host must poll the device (this happens deep in the stack)
- The host makes particular guarantees about data transmission, bandwidth, and latency to the device
- Generally only transmits small amounts of data (e.g. max 8 bytes for Low Speed, 1024 bytes for High Speed)

### Isochronous transfers

- Real-time, continuously streaming data
- Used for things like webcams and audio, where if the data is old it's useless and so dropped
- Not supported by nodes libusb implementation

### Bulk transfers

- Used for bursts of large amounts of data
- Built in error correction
- Guaranteed delivery, but not bandwidth or latency
- Not for use in real-time/time sensitive applications
