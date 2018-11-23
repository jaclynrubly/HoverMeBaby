A Pen created at CodePen.io. You can find this one at https://codepen.io/jrubly/pen/gQzgVL.

 Taking an old library of ours and converting it to a web component.

Change parameters for the emitter in the data-config attribute, this should be formatted as a JSON string, like so:
```
'{"momentum" : 7, "numParticles": 50}'
```

The web component takes the following parameters:

- *momentum*
  - This determines the initial momentum factor for all of the particles. 5 is normal(ish) 10 is really forceful, and 100 is stupid.
  - default 5
- *gravity*
  - The gravity to add to each particle in pixels, every frame.
  - default 0.4
- *friction*
  - How much friction to apply (as a multiplicant) to the particles' motion. Should not exceed one.
  - default 0.999
- *numParticles*
  - The number of particles to add on each hover.
  - default 20
- *numUniqueParticles*
  - The number of particle classes to add. This determines the particle originality.
  - default 5
- *scaleInitial*
  - Determine the initial scale factor for the particles before randomisation. 0 is nothing, 1 is 100%.
  - default 0.5
- *scaleFactor*
  - Determines how much randomness to add to each particle.
  - default 0.8
- *removeAt*
  - Determines the point, in scale, at which the particle is removed.
  - default 0.05
- *extraStyles*
  - This is a style string to apply to the elements inside the shadow dom. This is mainly used when you want to style the particles.
  - default ''
- *triggerAtMouse*
  - This determines whether the particles spawn at the position of the user's mouse as they hover over the element.
  - default false

## Try one of these configs

### Some emojii!
```
<div class="button" is="wtc-barfy-stars" data-config='{"scaleInitial": 1, "momentum" : 7, "numParticles": 100, "extraStyles" : ".BSParticle::after { background: url(\"https://s3-us-west-2.amazonaws.com/s.cdpn.io/982762/nauseated-face_1f922%20(1).png\") no-repeat center center; background-size: contain; }.BSParticle--2::after { background-image: url(\"https://s3-us-west-2.amazonaws.com/s.cdpn.io/982762/leafy-green_1f96c.png\");}.BSParticle--3::after { background-image: url(\"https://s3-us-west-2.amazonaws.com/s.cdpn.io/982762/trex_1f996.png\");}.BSParticle--4::after { background-image: url(\"https://s3-us-west-2.amazonaws.com/s.cdpn.io/982762/dragon-face_1f432.png\");}.BSParticle--5::after { background-image: url(\"https://s3-us-west-2.amazonaws.com/s.cdpn.io/982762/crocodile_1f40a.png\");}"}'>Hover me, baby.</div>
```

### Lots of particles!
```
<div class="button" is="wtc-barfy-stars" data-config='{"scaleInitial": 1, "momentum" : 10, "gravity": 0.4, "friction": 0.9999999, "numParticles": 100}'>Hover me, baby.</div>
```

### Zero gravity particles
```
<div class="button" is="wtc-barfy-stars" data-config='{"scaleInitial": 1, "momentum" : 10, "gravity": 0, "friction": 0.9999999, "numParticles": 100}'>Hover me, baby.</div>
```

### Particles that trigger at the position of the mouse
```
<div class="button" is="wtc-barfy-stars" data-config='{"numParticles": 20, "gravity": 0.2, "triggerAtMouse": true}'>Hover me, baby.</div>
```