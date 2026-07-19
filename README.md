# Orbital Transfer Visualization and Mission Optimization

## Objective
This project studies orbital transfers between circular orbits and gradually builds from basic trajectory visualization toward mission-level optimization. It visualizes transfer geometry, computes delta-v and transfer time, compares alternative transfer strategies, and estimates propellant mass under simple mission constraints.

The current notebook is organized as a layered analysis. Early layers focus on orbital mechanics and plotting; later layers connect transfer strategy, propulsion efficiency, operational constraints, and mission decision making.

## Current Scope
The project currently includes:

- Hohmann transfer calculations between circular orbits
- visualization of initial orbit, target orbit, central body, and transfer ellipse
- delta-v component plots and total delta-v budget
- parameter sweeps over target orbit radius ratios
- 2D delta-v heatmaps / contour plots over orbit-radius design space
- transfer time vs delta-v tradeoff visualization
- comparison of Hohmann, bi-elliptic, and low-thrust spiral transfers
- simplified low-thrust spiral modeling with assumed acceleration
- Mars mini mission optimization using propellant mass as the objective
- rocket-equation-based propellant estimates using specific impulse
- simple mission constraints for transfer time, power availability, and operational risk

## Notebook Layers

### Layer 1: Hohmann Transfer Baseline
Computes and visualizes a basic two-burn Hohmann transfer. This layer introduces the main physics quantities used later: circular velocity, transfer-orbit velocity, delta-v components, transfer ellipse geometry, and transfer time.

### Layer 2: Parameter Space and Tradeoff View
Sweeps orbit radius ratios to show how transfer cost changes as the target orbit moves farther away. This layer includes delta-v curves, transfer-time curves, heatmaps, and a Pareto-style time / delta-v view.

### Layer 3: Alternative Transfer Strategies
Compares three transfer approaches:

- Hohmann transfer
- best bi-elliptic transfer
- low-thrust spiral transfer

The comparison includes both geometry plots and strategy-family curves for total delta-v and transfer time.

### Layer 4: Mini Mission Optimization
Defines a simplified Mars satellite mission:

- start from low Mars orbit
- transfer to a higher communication orbit
- minimize propellant mass
- satisfy simple constraints on time, power, and operational risk

This layer uses the rocket equation to convert delta-v into propellant mass and compares feasible transfer strategies under mission assumptions.

## Tools

- Python
- NumPy
- Matplotlib
- Jupyter Notebook
- Git/GitHub

## Project Structure

- `notebooks/`: experiments, analysis, and visualizations
- `src/`: future home for reusable orbital mechanics and plotting functions
- `figures/`: exported plots and visual assets

## Possible Extensions

- move stable notebook functions into `src/`
- add plane-change maneuvers and inclination constraints
- improve low-thrust modeling with numerical propagation
- include payload mass and propulsion-system dry mass
- add more realistic mission constraints such as launch windows or communications geometry
- build an interactive website with sliders for orbit radii, propulsion type, power, time limits, and mission constraints
- extend the project toward solar-system visualization and constellation optimization

## Status
This is an early-stage research and visualization project. The notebook is currently the main workspace, and the models are intentionally simplified so the physical tradeoffs remain easy to inspect and explain.
