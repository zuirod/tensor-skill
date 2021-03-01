# tensor-skill

Dominion is a game where a small advantage early on can snowball into a decisive advantage. As such, your opening buys (i.e., the cards you buy in the first two turns of the game) are very important in laying the foundation for your strategy throughout the rest of the game.

This is the sequel to [bskull-openings](https://github.com/zuirod/bskull-openings), in which the TrueSkill rating system was used to rank openings in the [bskull-openings dataset](https://github.com/zuirod/bskull-openings/tree/main/data) by considering matches between openings as a 1 vs 1 game. In reality, each opening is made up of cards, so it is more appropriate to consider matches between openings as a team vs team game, allowing the model to generalize to openings not in the dataset. 

TrueSkill is capable of modeling such games, but is based on the assumption that the skill of a team is the sum of the skills of its players. This assumption does not hold in this setting, so a latent factor model, explicitly modeling the cards and diminishing marginal utility, was used to assess the quality of different openings better than the TrueSkill rating system.

If you are not familiar with dominion, learn to play for free at [Dominion Online](https://dominion.games/).

## Usage
You can simply view in your browser: [How To Base Dominion Opening, Part 2](https://github.com/zuirod/tensor-skill/blob/main/How%20to%20Base%20Dominion%20Opening%2C%20Part%202.ipynb).

For those who would like to dig through the code, install the requirements below, then run the following command at the Terminal (Mac/Linux) or Command Prompt (Windows):

```jupyter notebook```

A browser window should open. Wait for the page to load, then click 'How to Base Dominion Opening, Part 2.ipynb'. Click Kernel > Restart & Run All to run all the cells, or Shift + Enter to run an individual cell.

## Requirements

Run the appropriate commands at the Terminal (Mac/Linux) or Command Prompt (Windows).

### Install with conda

If you have [Anaconda or Miniconda](https://docs.conda.io/projects/continuumio-conda/en/latest/user-guide/install/index.html) installed, run:

Create a conda environment:

```conda create --name tensor-skill --file requirements.txt```

Activate the environment:

```conda activate tensor-skill```

### Install with pip

Alternatively, if you have [Python](https://www.python.org/downloads/) installed, run:

```pip install notebook pandas trueskill matplotlib tensorflow lxml scikit-learn```
