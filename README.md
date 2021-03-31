# PredatorPrey
 
## WHAT IS IT?

The application simulates a simple Prey-Predator ecosystem. The model has two types of agents: a Prey agent represented by a green cow, and a Predator agent represented by a red wolf.

## HOW IT WORKS

ENVIRONMENT - The environment is a 2D space filled with patches. 
1. Each patch can either be filled, represented by the color green, or empty, represented by the color black.
2. Each patch has a `life` value, which starts at zero. If the patch is empty (black), it's `life` value increases. Once its `life` value is equal to a set `growth` value, the patch becomes green, and the `life` value is set to zero.


AGENTS - The model is populated by agents which interact with the environment and each other.
1. All agents wander around randomly in the environment. 
2. Each agent starts with a set amount of `energy` which is reduced each time they move around. Once the `energy` of the agent is reduced to zero, it dies. 
3. Each agent has a chance to `reproduce`. When an agent reproduces, a new agent of the same type is created at the same location of the agent that reproduced.

PREY - The `Prey` agent consumes filled patches (green) to gain energy. After a `Prey` agent consumes a filled patch, it becomes empty (black)

PREDATOR - The `Predator` agent consumes `Prey` agents located in the same patch. It gains energy for each `Prey` agent it consumes. Once a `Prey` agent is consumed, it dies.

## HOW TO USE IT

To run the model, just click the `Setup` button, then the `Run` button.

SLIDERS
1. Max Turn - The maximum degrees each agent turns per tick.
2. Max Step - The maximum distance each agent moves per tick.
3. Growth Rate - The amount of time before an empty patch becomes filled. A growth rate of zero indicates that patches never become filled. A higher number equals more time before a patch becomes filled again.
4. Population - The initial population of a certain agent type.
5. Reproduction Rate - The chance each agent has of reproducing each step. A higher number equals a higher chance.
6. Starting Energy - The initial energy each agent starts with once it is born.

GRAPHS
1. Total Population - Plots the total population of every `Prey` (blue) and `Predator` (red)
2. Total Energy - Plots the total energy of every `Prey` (blue) and `Predator` (red)

## THINGS TO NOTICE

1. Predators never win - Unless the growth rate exceeds the amount of energy consumed, the `Predators` could never reach a stable population as they consume all of their sources of energy
2. Stable Prey Population - The population of the `Preys` could reach a point where it becomes stable - the population of `Preys` does not increase nor decrease after a certain point.
3. Total Extinction - If the reproduction rate is too low, both agents will lose all their population and become extinct

## THINGS TO TRY

Try to find a set of values where an equilibrium is reached, where the number of `Predators` and `Preys` are stable.

## EXTENDING THE MODEL

Smarter Agents - Currently, the movements of both agents are random. An extension of the model could include agents that move torwards sources of energy.

## RELATED MODELS

The base of the model was based on the `Ants` model discussed in class.

## CREDITS AND REFERENCES

Thank you Sir Briane for the `Ants` model.