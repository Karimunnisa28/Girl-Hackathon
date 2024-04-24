# Girl-Hackathon
Introduction
This README provides instructions on setting up and running the code for instantiating a mesh network with routers adjusted to meet specified requirements such as buffer size, latency, bandwidth, and throttling percentage.

Environment Setup
To run the code, ensure you have the following environment set up:

Hardware Description Language (HDL) development environment compatible with the language used in the code (e.g., Verilog, VHDL).
Module Parameters
BUFFER_SIZE: Size of the buffer in each router.
MESH_SIZE_X and MESH_SIZE_Y: Dimensions of the mesh network.
MIN_LATENCY: Minimum latency requirement.
MAX_BANDWIDTH: Maximum bandwidth requirement.
THROTTLING_PERCENTAGE: Throttling percentage for bandwidth control.
      3.Generating the Environment
Define the module parameters as listed above.
Calculate BUFFER_SIZE_ADJUSTED based on the specified occupancy requirement of 90%.
Running the Code
Instantiate the mesh module, representing the mesh network.
     4.Inside the mesh module:
Declare inputs (clk, rst, is_onoff_i, is_allocatable_i, data_i, is_valid_i) and outputs (error_o, data_o, is_valid_o, is_onoff_o, is_allocatable_o).
Loop through each row and column of the mesh network.
Instantiate a router module (router_inst) for each position in the mesh network, passing parameters (BUFFER_SIZE_ADJUSTED, MIN_LATENCY, MAX_BANDWIDTH, THROTTLING_PERCENTAGE).
     5.Inside each router instantiation:
Define connections to the router, including clock and reset signals, input and output data signals, and control signals such as allocation and validity.
End the module definition
