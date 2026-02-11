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

1. **Clone this repository.**

2. **Configure vanetza-nap:**
   Navigate to your local `vanetza-nap` repository and replace the following files with the versions provided in this repository:
   * Replace `vanetza-nap/docker-compose.yml`
   * Replace `vanetza-nap/tools/socktap/config.ini`

3. **Start the environment:**
   Go back to the `vanetza-nap` root directory and run:
   ```bash
   docker-compose up
   ```
   
4. Run a Single Simulation: Navigate to the V2X folder and run:
   ```bash
   python3 main.py
   ```
   Note1: In config.py it is possible to switch between the default SUMO behavior (BASELINE) or SUMO with Python script interaction (V2X).
   Note2: In config.py it is possible to change the seed parameter
   
6. Run Multiple Simulations: To run consecutive simulations, execute:
   ```bash
   python3 batch_run.py
   ```
   Note: Inside this file, it is possible to change the random seed and the number of vehicles.

