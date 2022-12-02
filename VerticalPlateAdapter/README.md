# Vertical plate adapter for OT labware

## What is it?
We're talking about a labware adapter to be used with the Opentrons OT2 robot

## Why a vertical labware adapter?
We want to use a normal 96-well plate rotated of 90° in order to work in the center of the plate without loosing tips and time.
This expecially useful working with the Opentrons Thermocycler to decrease samples evaporation.

## 3D model
You'll find two different 3D models that can be used in 4 configuration:
1. top-left corner alignmen (adapter 1)
1. top-right corner alignment (adapter 2)
1. bottom-left corner alignment (adapter 2)
1. bottom-right corner alignment (adapter 1)

Here some explanation images:

![Top-left alignment](assets\top-left-slot-4.png)
![Top-right alignment](assets\top-right-slot-4.png)
![Bottom-left alignment](assets\bottom-left-slot-1.png)
![Bottom-right alignment](assets\bottom-right-slot-1.png)

### Important note: 
### The labware is seen by OT as a normal labware occupying the assigned slot only. Please carefully check your labware disposition.

## Labware generator
In the *custom_labware_generator* folder you'll find the python script used to generate the labware definitions.

## How to use labware definitions
Labware definitions are given in JSON format. You have multiple way to load them:
1. upload the definitions on the robot using the OT App and than use them in protocols as normal labware;
2. load the labware file on the robot, load the JSON from the file and than call `ProtocolContext.load_labware_from_definition`