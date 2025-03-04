+++
title = "Position Based Dynamics"
date = "2025-03-04T04:09:43-07:00"
draft = false
+++

<style type="text/css">
    .center {
        text-align: center;
    }

    .center img {
        display: block;
        margin: 0 auto;
        width: 80%;
    }
</style>

## Definition

> Position-Based Dynamics (PBD) doesn’t rely on Newton’s laws of physics. Instead, it adjusts the positions of objects to satisfy rules (constraints)—like preventing them from overlapping or stretching too much. It’s simple, fast, and ideal for simulating cloth, soft bodies, or fluids, where stability matters more than exact physics.

## Example: Strings Connecting Particles

PBD is perfectly suited for this type of simulation. Imagine one particle pinned in place and a second particle hanging by a string. PBD keeps the distance between the two particles constant by making small corrections over multiple steps. If the connection stretches beyond its initial length, PBD shortens it by moving the hanging particle slightly toward the pinned one. The vertical movement of the particle is determined by calculating its velocity over time. Then, PBD takes over, adjusting its position to maintain the correct distance from the pinned particle.

[PBD Repository](https://github.com/MehrdadDw/position-_based_dynamics "PBD's Homepage"), [Simulation GIF](https://raw.githubusercontent.com/MehrdadDw/position-_based_dynamics/main/simulation.gif)

## Visualization

Here’s an example of PBD in action:

{{< figure src="https://github.com/MehrdadDw/myblog/blob/main/static/images/simulation.gif?raw=tru?raw=true" alt="PBD Simulation of Particles Connected by a String" class="img-responsive" >}}

{{< figure src="https://github.com/MehrdadDw/myblog/blob/main/static/images/pbd-correction.jpg?raw=tru?raw=true" alt="PBD Correction" class="img-responsive" >}}

## Question

Look at the middle pair of particles—shouldn’t the string behave like a flexible thread? Instead, it looks like a solid, rigid connection! How can this be fixed?
