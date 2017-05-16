## PID Controller

### P - Proportional

The proportional term makes the system minimize the error. In this case, the Cross-Track Error which is the distance between the car and the middle of the road. However, the problem with the P term is that by itself it doesn't handle the speed and inertia of the vehicle. This makes the system to then constantly overshoot left and right of the middle of the road.

### D - Derivative

The derivative takes into account the difference of the current and previous error in an attempt to slow down as the system reaches minimum error. This allows the system to stabilize as it approaches the center effectively reducing the overshooting issue described before.

### I - Integral

Finally, the integral is the cummulative error and it usually correct for small drifts and issues the vehicle may have. For our particular project the integral was set to a very small number, and it would not be surprising if we didn't really needed in the first place. The fact is that in the simulator there might not be difting at all, still a very small value seem to improve thing a bit.

## Hyper-parameters

I actually tuned these values manually. Zeroing out the D and I, I started with the P term until it did an OK job. Once the P controller was able to drive some, I then added the D tuned it and then the I and tuned it. Ideally, I would have implemented twiddle or some other method, but I was running out of time. Next project I should try something slightly different.

## Video

[![Alt text](https://img.youtube.com/vi/LQjUI-mwxss/0.jpg)](https://www.youtube.com/watch?v=LQjUI-mwxss)
