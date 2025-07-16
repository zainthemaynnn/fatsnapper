# fatsnapper
`fatsnapper` is a CCD camera built from scratch.

## motivation
most stuff I have here on github is software I've developed throughout work and high school by myself for fun, but three things have occurred to me:

- I've done two years of EE courses
- my internship just got me a hell of a lot of money
	- which I have quickly blown on oscilloscopes, protoboards, 3D printers, MCU's...
- I thirst to return to rust programming

so, it's about time I did some actual electrical engineering.

since I have been working a lot with cameras lately, we have `fatsnapper`.

## plans
there are already plenty of cheap CMOS detectors online, which you can access through MIPI or other serial protocols. that said, I'm planning on focusing more on the electrical internals of a detector, not embedded. this project will be including its own readout circuitry, which is usually included on the imaging sensor itself as part of the chip.

since I can't just produce my own active pixel sensor array because I unfortunately don't own a semiconductor fabrication facility yet, `fatsnapper` is just going to use an array of typical fat photodiodes (hence the name `fatsnapper`). besides this, the logic should be pretty similar to a typical CCD (a camera is just a bunch of miniature photodiodes), but I do expect there to be some challenges due to its size.

after the analog (difficult) readout part is done, I will implement some additional digital processing which is also done on most imaging sensor chips. it may be wired, or I'll grab some FPGA that I bought if that gets too bulky.

as an end goal, it will hopefully be accessible through some CPU. for the hell of it, I may use something fancy like PCIE for that, but it's long in the future.

`fatsnapper` WILL be extremely slow and WILL exhibit terrible resolution, but that's the charm.
