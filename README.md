NEAT Visualizer

Background and Project Details
This project provides dynamic visualizations for analyzing the behavior and evolution of neural networks using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm. The core aim is to track how the population of networks evolves over time, how species diverge, and how network topologies change, all while offering optional biological realism through spiking neuron modeling.

Visualizations are implemented using Matplotlib and Graphviz. The plots can be saved or rendered live during training. This is especially useful when debugging or presenting evolutionary behavior in real-time.

Functional Overview
1. Fitness Evolution Plot
   Plots the average, best, and standard deviation of fitness values across generations.

   X-axis: Generation number

   Y-axis: Fitness score

   Helps detect stagnation, convergence, or improvement patterns

   Standard deviation bands (+1σ, −1σ) show population variance

2. Species Distribution Plot
  Tracks how NEAT's speciation mechanism maintains diversity.
  
  Stacked area chart showing the number of genomes in each species over time
  
  Each colored layer represents a species
  
  Useful for debugging if a single species dominates too early or if diversity collapses

3. Neural Network Topology Visualization
   Draws the genome’s neural architecture with optional pruning of unused nodes.

   Node colors: Gray (input), Blue (output), Customizable hidden nodes

   Arrow thickness reflects connection weight

   Red arrows: Positive weights; Blue arrows: Negative weights

Dotted arrows indicate disabled connections

Can hide nodes with no input/output relevance for simplicity

4. Spiking Neuron Visualization
Simulates an Izhikevich spiking neuron model and shows its dynamics.

4 plots: Membrane potential, spike events, recovery variable (u), and input current (I)

Time-series simulation of realistic spiking behavior

Useful for neuroscience-inspired AI models or debugging SNN-based systems

Inputs and Compatibility
Designed to work with:

statistics object from NEAT-Python (for fitness and species data)

Genome and config objects (for topology rendering)

External input current data (for neuron simulation)

Each visualizer can be called independently and customized via function arguments such as log_scale, prune_unused, show_disabled, and more.

Optional Parameters
log_scale: Enables logarithmic y-axis scaling

show_disabled: Includes disabled connections in network graphs

prune_unused: Removes inactive nodes from topology diagrams

view: Toggle between live display and file saving

node_names: Custom labels for input/output nodes

