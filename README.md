# **NBA 2022-23 predictions**

<p style="display: flex; align-items: center;">
    <img src="images/nba.png" alt="NBA Logo" style="width: 200px; height: auto; margin-left: 0px;">
</p>

## 1. Repository introduction

This repository was created as a project for the Visualization course in the Big Data Master's Degree at Comillas ICAI University. The objective was to create a storytelling by developing 8 visualizations in Python using different libraries. In my case, I developed a storytelling that predicts the following outcomes for the NBA 2022-23 season:

- Eastern and Western Conference finals
- NBA finals
- NBA champions
- MVP

The libraries used for visualization were:

- `Matplotlib`
- `Seaborn`
- `Bokeh`
- `Plotly`
- `Folium`

The datasets used can be found in the following [Kaggle link](https://www.kaggle.com/datasets/sumitrodatta/nba-aba-baa-stats). However, since not every table was used,  I have included only the necessary ones in the `data` directory. Additionally, a `csv` file with the US cities (`data/usa_cities.csv`) was used to obtain the longitude and latitude of NBA teams' cities, which was necessary to plot the first visualization (a US map with each team's logo in its corresponding city).

## 2. Code structure

The repository is structured as follows:

### 2.1. `data`

This directory contains:

- `usa_cities.csv`: `csv` file with the longitudes and latitudes of US cities.
- NBA datasets:
  - `Advanced.csv`
  - `Opponent Stats Per Game.csv`
  - `Player Per Game.csv`
  - `Team Abbrev.csv`
  - `Team Stats Per Game.csv`
  - `Team Summaries.csv`

### 2.2. `notebooks`

This directory contains the Jupyter notebook with the developed code.

### 2.3. `config`

This directory contains a `YAML` configuration file with dictionary for each team, which includes the following information:

- **Conference**: used for segmenting some plots into Western and Eastern conferences.
- **Color**: used to assign custom colors to each team.
- **URL**: necessary to get teams' logos, which were used for the first visualization.

This information was required for some of the visualizations, but was not included in the datasets. Therefore, I added this information to the config file.

### 2.4. `images`

This directory contains the following image files:

- `nba.png`: NBA logo in PNG format, used as a header image for the README and the Jupyter notebook.
- `NBA_logos`: a directory containing each NBA team's logo, used in a visualization to display the teams' logos on a map.
- `players_photos`: a directory containing several NBA players' photos, used in a visualization to display player statistics.

## 3. Environment installation

To create the required environment, execute the following command:

#### `environment.yaml`

````bash
conda env create -f environment.yaml
````

#### `requirements.txt`

````bash
pip install -r requirements.txt
````