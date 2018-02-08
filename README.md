# scaler

**Scaler** is a simple bash interpretor useful when working on **scale conversions**. A calculator makes those simple calculations very teddious, not with scaler.

It requires `bc` to work.

## Example 1: work between a map and a real distance

We might be working on some sketches and need a quick calculator. 

For instance, a wall measures 187cm for real, while it's 11mm on the map.

```bash
~$ scaler 11mm 187cm

Scale set to 11mm:187cm
Default unit set to cm, type mm to change to that default unit.
Now looping through measures ('exit' or Ctrl-C to exit)...

cm> 59
 --> 3.47mm

cm> 4mm
 --> 68.00cm

cm> mm
mm> 59
 --> 1003.00cm

mm> exit
```

The unit is optional whenever it is the same as shown in the prompt. 

To switch default unit from cm to mm, we simply typed "mm".

## Example 2: conversion between units

This necessitates GNU units (the `units` command), which is installed with some Linux distributions. GNU units knows hundreds of units for distance, weight etc and **scaler** can use it to get the ratio between two homogenous units:

```bash
~$ scaler miles km

Scale is 0.62137119miles:1km
Default unit set to km, type miles to change to that default unit.
Now looping through measures ('exit' or Ctrl-C to exit)...

km> 10
 --> 6.21miles

km> 10miles
 --> 16.09km

km> miles
miles> 10
 --> 16.09km
```

That's all folks.
