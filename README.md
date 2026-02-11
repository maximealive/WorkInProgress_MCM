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
   
4. **Run a Single Simulation** -> navigate to the V2X folder and run:
   ```bash
   python3 main.py
   ```
   > Note: Edit config.py to:  
   > * Switch SIMULATION_MODE between BASELINE (default SUMO) and V2X (Python interaction).  
   > * Change the seed parameter.
   
5. **Run Multiple Simulations**-> navigate to the V2X folder and run:
   ```bash
   python3 batch_run.py
   ```
   > Note: Inside this file, it is possible to change the random seed and the number of vehicles.

## ToDo
- Implement all MCM messages

## References
- ETSI EN 302 637-2 V1.3.1 (2014-09)
- ETSI TR 103 578 V2.1.1 (2024-04)

### Tools & Libraries
* **[Vanetza](https://github.com/nap-it/vanetza-nap)** - The open-source implementation of the ETSI C-ITS protocol suite used in this project.
* **[Eclipse SUMO](https://www.eclipse.org/sumo/)** - Simulation of Urban MObility, used for traffic generation.

### Documentation & Standards
* **[ETSI ITS Standards](https://www.etsi.org/technologies/automotive-intelligent-transportation)** - Standards for Intelligent Transport Systems (V2X).
* **[Docker Documentation](https://docs.docker.com/)** - Reference for container deployment.

