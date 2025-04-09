# KPG Instance Files

This folder contains synthetic instances for the **Knapsack Potential Game (KPG)**, generated using the Python script adapted from the original C++ version by Dragotto and Scatamacchia (2023):
> https://github.com/gdragotto/ZeroRegretsAlgorithm/blob/main/instance_generators/instances_kp/generator.cpp
 
## Folder Structure

Each subfolder `type_A`, `type_B`, and `type_C` corresponds to a different **interaction type**:

- **Type A (Potential Game)**: Shared interaction values between players.
- **Type B**: Random positive interactions.
- **Type C**: Random negative interactions (∈ [−R/5, 0]) to ensure feasibility in large-scale instances.

## File Format

Each instance file follows this format:

Line 1: <number_of_players> <number_of_items>  
Line 2: <budget_1> <budget_2> ... <budget_n>  
Line 3+: <item_id> <profit_1> <weight_1> ... <profit_n> <weight_n> <C_ij values for all i ≠ j>  

- Each item line begins with its index, followed by:
  - Profit and weight for each player.
  - Interaction values `C_ij` for all player pairs (i ≠ j), listed in row-major order.
