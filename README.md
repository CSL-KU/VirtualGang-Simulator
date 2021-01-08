The simulator has been tested with Python-2.7. It may / may not work with
Python-3.

## Required Packages
The following packages are required to run the simulator:
  - z3 v4.8.9 - 64 bit (Download from: https://github.com/Z3Prover/z3/releases)
  - matplotlib (sudo apt install python-matplotlib)
  - colorama (pip2 install colorama)

Colorama is used to stylize the output messages from the simulator. It is not
*required* (raw messages will be printed) but is recommended.

## How to Run?
Use the following command to see the options for configuring / running the simulator:
```bash
./simulator -h
usage: simulator.py [-h] [-p | -d] [-v] [-t {light,mixed,heavy}]
                    [-n {1,10,100,1000}] [-e {0,25,50,75}] [-r {0,r}]
                    [-m {4,8,16,32}] [-N {4,8,10,12}]

optional arguments:
  -h, --help            show this help message and exit
  -p, --pristine        collect pristine data
  -d, --demo_mode       illustrate the simulation steps with an example run
  -v, --verbose         specify output verbosity
  -t {light,mixed,heavy}, --taskset_type {light,mixed,heavy}
                        type of taskset
  -n {1,10,100,1000}, --num_of_tasksets {1,10,100,1000}
                        number of tasksets to generate for each util. point
  -e {0,25,50,75}, --edge_probability {0,25,50,75}
                        edge probability in generated tasksets
  -r {0,r}, --demand_type {0,r}
                        type of resource demand
  -m {4,8,16,32}, --core_count {4,8,16,32}
                        number of cores 'm' for the simulation
  -N {4,8,10,12}, --tasks_per_period {4,8,10,12}
                        max. number of tasks in any candidate-set
```

There is a **demo mode** of the simulator which illustrates the steps of the simulation using default parameters. To try that, run the simulator as follows:
```bash
./simulator -d
```
