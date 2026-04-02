Adaptive Rocket Landing Simulation: PID vs. RCGF
This repository contains a Python-based comparative study evaluating a standard baseline controller against a gated resilient framework. The simulation models a vertical rocket landing under identical dynamic conditions to evaluate performance under resource constraints and system stress.  
Simulation Scenarios
The implementation provides three distinct ways to analyze landing performance:
• Standard PID Baseline: Models a vertical landing using a traditional controller with anti-windup logic to manage altitude and velocity errors.  
• RCGF Gated Landing: Enables the Resource-Constrained Gating Framework (RCGF) to throttle the controller based on fuel availability and system stress.  
• Environmental Disturbance & Safety: Features a downward gust disturbance between t=5 s and t=7 s, with real-time monitoring to ensure thrust does not exceed structural limits.  
Flight Telemetry & Signals
The simulation tracks and visualizes four critical real-time signals:
• Altitude (m): Tracks the descent from an initial 100 m height to touchdown.  
• Velocity (m/s): Monitors descent speed and evaluates the "soft landing" capability upon contact.  
• Thrust Output (N): Visualizes how the RCGF "gates" the PID signal to stay within safety and hardware capacity envelopes.  
• Fuel Mass (kg): Records depletion from a maximum of 30 kg and demonstrates throttle reduction as fuel reaches critical levels.  
Credits & Legal Notice
Author: Kyle Harrison
Organization: Platinum Castles Inc.  
Copyright (c) 2026 Kyle Harrison. All rights reserved.  
Unauthorized copying, distribution, or use of this code, in whole or in part, for commercial or public purposes is strictly prohibited.
esource-Constrained Gating Framework (RCGF)
The Resource-Constrained Gating Framework (RCGF) acts as an intelligent supervisor for rocket landing dynamics, using a dedicated gating layer to manage control efforts based on real-time feedback and PID variables. By dynamically adjusting thrust and orientation commands, the system ensures high-precision stability and optimizes performance even within strict hardware and environmental limitations.
Central to this architecture is the "Truth Anchor"—a state estimator that maintains a consistent "mental map" of physics. Rather than chasing sensor jitter or bad data, the RCGF validates every measurement against expected dynamics, allowing the craft to maintain a stable trajectory through high winds, thermal stress, and signal noise. This transition from reactive correction to predictive validation represents a shift toward more resilient, autonomous aerospace recovery.
What this version adds:
• The "Truth Anchor" Branding: It introduces your specific terminology for how the system filters noise.
• Adverse Conditions: It mentions high winds and thermal stress, giving the "Resource-Constrained" part of the name more tangible stakes.
• Predictive vs. Reactive: It highlights the "intellectual" side of the supervisor, moving beyond simple PID loops.
