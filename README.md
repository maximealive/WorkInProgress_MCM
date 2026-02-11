# WorkInProgress_MCM

## Software
- SUMO (Version 1.12.0)
- python3 (Version 3.10.12)
- vanetza-nap (https://github.com/nap-it/vanetza-nap)
- WSL (Version: 2.6.3.0) - Ubuntu-22.04
- Docker (Version 29.2.1)

## Getting Started

### Prerequisites

1. **WSL** (Windows Subsystem for Linux)  
   [Install Guide](https://learn.microsoft.com/en-us/windows/wsl/install)

2. **SUMO** (Simulation of Urban MObility)  
   [Install Guide](https://sumo.dlr.de/docs/Installing/index.html)

3. **Docker + Vanetza-NAP** See the `README.md` file in the `vanetza-nap` repository.

### Usage
1) Download this repository
2) When clone vanetza-nap's repository navigate to the project's root directory folder and substitute: vanetza-nap/docker-compose.yml + vanetza-nap/tools/socktap/config.ini with the files present in this repository
3) Go back to vanetza-nap's repository root directory and run: docker-compose up
4) For single simulation go to V2X folder and run: python3 main.py (in config.py is possible to have the default SUMO behaviour - BASLINE, or SUMO with the interaction with the pyton script - V2X)
5) For multiple consecutively simulations run: batch_run.py (in this file is possible to change seed and number of vehicles)

### Usage

1. **Clone this repository.**

2. **Configure vanetza-nap:**
   Navigate to your local `vanetza-nap` repository and replace the following files with the versions provided in this repository:
   * Replace `vanetza-nap/docker-compose.yml`
   * Replace `vanetza-nap/tools/socktap/config.ini`

3. **Start the environment:**
   Go back to the `vanetza-nap` root directory and run:
   ```bash
   docker-compose up
4. Run a Single Simulation: Navigate to the V2X folder and run:
   ```bash
   python3 main.py



