# Fifa_Dataset_Analysis
Machine learning pipeline to predict FIFA17 player positions and potential growth from player attributes.
# FIFA17 Player Analysis: Position & Potential Growth Prediction

## Overview
This project uses the FIFA17 dataset to build a **combined machine learning pipeline** that predicts:

1. **Player Position** – Best playing position (e.g., ST, CAM, GK) based on player attributes.
2. **Potential Growth** – Whether a player is likely to improve significantly in the future.

The project includes **exploratory data analysis (EDA)**, feature importance visualization, and a ready-to-use function for predictions.

---

## Dataset
The dataset contains FIFA17 player data with features like:
- Skill attributes (Dribbling, Passing, Shooting, Tackling, Reflexes, etc.)
- Personal attributes (Age, Potential, Overall, Work Rate, Reputation)

Source: FIFA17 dataset in CSV format.

---

## Features Used

### Position Classification
Numeric attributes like:
- Crossing, Finishing, Dribbling, Ball Control, Sprint Speed, Agility, Reactions, etc.

### Potential Growth
- Age, Overall, Potential, International Reputation, Weak Foot, Skill Moves, and key skills.

---

## Model
- **Random Forest Classifier** for both tasks:
  - Multi-class classification for Position
  - Binary classification for Potential Growth

---

## How to Use

```python
from predict_player import predict_player_stats

# Example: Predict for a sample player
sample_player = df.iloc[0].to_dict()
position, growth = predict_player_stats(sample_player)
print("Predicted Position:", position)
print("Predicted Growth:", growth)
