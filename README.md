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
