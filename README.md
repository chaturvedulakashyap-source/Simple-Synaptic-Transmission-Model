# Simple-Synaptic-Transmission-Model
This project demonstrates basic synaptic transmission between two neurons using a leaky integrate-and-fire model. A presynaptic neuron is initialized above threshold and generates a spike, which produces a subthreshold depolarization in a postsynaptic neuron through a unidirectional synapse


# Synaptic Transmission Model using Brian2

## Overview
This project models basic synaptic transmission between two neurons using a leaky integrate-and-fire framework. It demonstrates how a presynaptic spike induces a postsynaptic voltage response without necessarily triggering firing.

## Model Description
- Two neurons simulated using first-order membrane dynamics  
- Equation: dv/dt = -v / τ  
- Threshold-based spiking with reset mechanism  
- Unidirectional synapse from neuron 0 → neuron 1  
- Synaptic event modeled as instantaneous voltage increment in the postsynaptic neuron  

## Simulation Setup
- Neuron 0 initialized above threshold → generates a spike at t ≈ 0 ms  
- Neuron 1 initialized at resting state  
- Synaptic weight set to a subthreshold value (0.5)  

## Key Results
- Presynaptic neuron generates an immediate spike  
- Postsynaptic neuron exhibits a transient depolarization  
- Voltage decays exponentially back to baseline  
- No postsynaptic spike occurs at this synaptic strength  

## Interpretation
This demonstrates subthreshold synaptic transmission, where input influences membrane potential but does not cross firing threshold. Increasing synaptic weight results in postsynaptic firing, illustrating threshold-dependent signal propagation.

## How to Run
```bash
pip install brian2 matplotlib
python synapse_model.py
