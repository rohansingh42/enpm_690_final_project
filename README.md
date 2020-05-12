# Autonomous Decision Making Dense Traffic
ENPM690 final project

# Dependencies
This project requires the following libraries:
- python3 
- pytorch
- tensorboardX

# Build instructions
First build the code using the following commands:
```
cd highway-env/
sudo python3 setup.py install
cd ../rl-agents/
sudo python3 setup.py install
```
# Run instructions
To train the dqn agent run the following command by navigating to the `rl-agents/scripts/` subdirectory:
```
python3 experiments.py evaluate configs/HighwayEnv/env.json configs/HighwayEnv/agents/DQNAgent/dqn.json --train --episodes=2000 --name-from-config
```

To train the agent using fitted Q iteration run the following command from the same subdirectory:
```
python3 experiments.py evaluate configs/HighwayEnv/env.json configs/HighwayEnv/agents/FTQAgent/baseline.json --train --episodes=2000 --name-from-config
```