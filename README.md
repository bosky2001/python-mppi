[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
### This repository is my attempt at implementing Model Predictive Path Integral Control. I have taken the setup from the original repository (https://github.com/MizuhoAOKI/python_simple_mppi) and implemented my own version in it.

# Simple MPPI Implementation with Python
Model Predictive Path-Integral (MPPI) Control [[G. Williams et al., 2018]](#references) is a promising sampling-based optimal control algorithm.  
This repository is for understanding the basic idea of the algorithm.

<img src="./media/mppi_pathtracking_obav_demo.gif" width="500px" alt="pathtracking and obstacle avoidance demonstraion">
<img src="./media/pendulum_swingup_demo.gif" width="500px" alt="swinging up pendulum demonstraion">

## Dependency

- [python](https://www.python.org/)
  - version 3.10 or higher is recommended.

- [poetry](https://python-poetry.org/)
  - seting up python environment easily and safely.
  - only `numpy`, `matplotlib`, `notebook` are needed to run all scripts in this repository.

- [ffmpeg](https://ffmpeg.org/)
  - mp4 movie writer
  - <details>
    <summary>installation details</summary>

    - For Ubuntu Users
        - `sudo apt-get update`
        - `sudo apt-get -y install ffmpeg`
    - For Windows Users
        - Install [scoop](https://scoop.sh/)
        - `scoop install ffmpeg`
    - For macOS Users
        - Install [homebrew](https://brew.sh/)
        - `brew install ffmpeg`
    - Check the official website if necessary
        - https://ffmpeg.org/

    </details>

## Setup
```sh
git clone https://github.com/MizuhoAOKI/python_simple_mppi.git
cd python_simple_mppi
poetry install
```

## Usage

### Path Tracking
<img src="./media/pathtracking.png" width="300px" alt="pendulum">

#### Simple Path Tracking
- Run simulation
    ```sh
    cd python_simple_mppi
    poetry run python scripts/mppi_pathtracking.py
    ```

- Run jupyter notebook if you would like to check mathematical explanations on the algorithm.
    ```sh
    cd python_simple_mppi
    poetry run jupyter notebook notebooks/mppi_pathtracking.ipynb
    ```

#### Path Tracking with Obstacle Avoidance
- Run simulation
    ```sh
    cd python_simple_mppi
    poetry run python scripts/mppi_pathtracking_obav.py
    ```

- Run jupyter notebook if you would like to check mathematical explanations on the algorithm.
    ```sh
    cd python_simple_mppi
    poetry run jupyter notebook notebooks/mppi_pathtracking_obav.ipynb
    ```

### Pendulum
<img src="./media/pendulum.png" width="300px" alt="pendulum">

- Run simulation to swing up a pendulum.
    ```sh
    cd python_simple_mppi
    poetry run python scripts/mppi_pendulum.py
    ```

- Run jupyter notebook if you would like to check mathematical explanations on the algorithm.
    ```sh
    cd python_simple_mppi
    poetry run jupyter notebook notebooks/mppi_pendulum.ipynb


## References
1. G. Williams et al. "Information-Theoretic Model Predictive Control: Theory and Applications to Autonomous Driving" 
    - URL : https://ieeexplore.ieee.org/document/8558663
    - PDF : https://arxiv.org/pdf/1707.02342.pdf
