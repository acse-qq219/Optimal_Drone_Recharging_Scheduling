# Notices
1. Output files of `1_data_generation.ipynb`:
	1. `inputs.csv` - Information of all sensor nodes
	2. `sub_path0.csv` -  Assigned sub path of single PDV after clustering algorithms (may have multiple files) **OPTIONAL**
	
2. Output file of `3_result_visualization.ipynb`:
	1. `complete_flight_path.gif` - The animation of complete flight path of all PDVs.  

3. There is no directory called `initial_guess\` can be found in `input\` because no actual initial guess files are uploaded. But users **SHOULD** create the directory!

4. The code uses `stderror` to detect errors when implementing I/O with files. This command may be unsafe and cause errors when building. Please turn off `SDL checks` in **C/C++ (Properties)**.

5. The C++ language standard is **ISO C++17 Standard**. Any older versions will lead to building errors. To use older versions (i.e. C++14), users should delete all commands related to `filesystem` and modify related file process logic, which is used to count the number of files in `output/sub_path/` directory.  

# Recent Updates
Source code of integrated system with user interface and ensemble test can be found in the folder `ensemble_system`. *Note that* There are two main classes. users need to uncomment codes according to comments. For ensemble test, hyper-parameters are set as:
- Minimum number of sensors to be recharged for single flight: 25
- Maximum number of neighbours to find when calculating initial guess solutions: 5
- Fitness metric factor for total recharged energy: 80 %
- Fitness metric factor for energy cost of the PDV: 20 %
- No consideration of fitness metric factor for PDV flight distances

- Genetic Computing:
	- Generations: 50
	- Populations: 50
	- Crossover Ratio: 50 %

- Black Hole Computing:
	- Generations: 50
	- Populations: 50
	- Attraction Ratio: 50 %

- Simulated Annealing Computing:
	- Initial temperature: 1e3
	- Minimum allowed temperature: 1e-4
	- Temperature reducing factor: 0.985
	- Populations: 50

