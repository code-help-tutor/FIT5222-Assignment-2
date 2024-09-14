# FIT5222 Planning and automated reasoning Assignment 2
## Pacman: Capture the Flag

Pacman Capture the Flag is developed by UC Berkeley CS188. It is a multiplayer 
capture-the-flag variant of Pacman. Two teams, blue and red, will compete with each other.
Each team needs to eat the food on the far side of the map while defending their own foods.
We will hold a Pacman Capture the Flag competition at the end of this semester.

### Part 1: Installation
Follow the instructions in [week 1](link) to get codes of Pacman : Capture the Flag.

### Part 2: Rules of Pacman: Capture the Flag
#### Characteristics
- An agent needs to trade off offense versus defense.
- Only limited information is provided to agents.

#### Layout
The Pacman map is now divided into two halves: blue (right) and red (left). Red agents (which all have even indices) must defend the red food while trying to eat the blue food. When on the red side, a red agent is a ghost. When crossing into enemy territory, the agent becomes a Pacman.

#### Scoring
- As a Pacman eats food dots, those food dots are stored up inside of that Pacman and removed from the board. 
- When a Pacman returns to his side of the board, he "deposits" the food dots he is carrying, earning one point per food pellet delivered.
- Red team scores are positive, while Blue team scores are negative.
- If Pacman is eaten by a ghost before reaching his own side of the board, he will explode into a cloud of food dots that will be deposited back onto the board.

#### Eating Pacman
- When a Pacman is eaten by an opposing ghost, the Pacman returns to its starting position (as a ghost). No points are awarded for eating an opponent.

#### Power Capsules
- If Pacman eats a power capsule, agents on the opposing team become "scared" for the next 40 moves, or until they are eaten and respawn, whichever comes sooner.
- Agents that are "scared" are susceptible while in the form of ghosts (i.e. while on their own team's side) to being eaten by Pacman.
- Specifically, if Pacman collides with a "scared" ghost, Pacman is unaffected and the ghost respawns at its starting position (no longer in the "scared" state).

#### Observations
- Agents can only observe an opponent's configuration (position and direction) if they or their teammate is within 5 squares (Manhattan distance).
- In addition, an agent always gets a noisy distance reading for each agent on the board.


#### Winning
- A game ends when one team returns all but two of the opponents' dots.
- Games are also limited to 1200 agent moves (300 moves per each of the four agents).
- If this move limit is reached, whichever team has returned the most food wins.
- If the score is zero (i.e., tied) this is recorded as a tie game.

### Part 3: Getting Started and Useful Tools
Use “git pull” to pull the latest code from [pacman-public repo](link).
You can find two examples in the Pacman Capture the Flag project. One is `baselineTeam.py`
and another is `team_pddl.py`.
`baselineTeam.py` is an official example for Pacman Capture the Flag. `team_pddl.py` is a simple example of how PDDL is used to guide Pacman's high-level actions. 

Important codes you should know in these examples:
- You can use the `ReflexCaptureAgent(CautureAgent)` class as a template for designing your own Pacman.
- `def chooseAction(self,gameState)`: This is the function that the game will call when it’s the agent’s turn to take action. In other words, where things start for each turn.
- `gameState`: This variable is an instance of GameState class (Defined in capture.py file) which contains the current state of the game and a set of useful functions for you to easily retrieve information of the current game state.

#### Important codes you should read:
- `GameState` class in capture.py: The instance of this class stores all the information about the current game state and a set of functions to retrieve information.
- `AgentState` in game.py: This class contains the state of an agent, which includes is Pacman, scared timer, food carrying.
- `CaptureAgent` class in captureAgents.py: This class is the base class of the agents you will implement.

### Part 4: Task
Your task will be to implement the Pacman agent/s to navigate the maze while eating food from the enemy’s home turf in `myTeam.py`. 
Your implementation should:
- Use PDDL to guide the high-level action of agents. You can   ```markdown
refer to `team_pddl.py` as a base implementation, and improve it by considering more states, introducing more high-level actions, and developing more complicated PDDL models.
- For each high-level action, you may improve the low-level implementation by introducing more features and weights to the model. 
- You should carefully consider for each high-level action what is the purpose of this high-level action and how you will award or penalize the agent.
- To train your Q-learning model, you can run pacman in silence mode with “-Q” argument and automatically run pacman for dozens of games with “-n 1000” argument. You can replace 1000 with another number you want. You also need to use “-l ./layouts/bloxCapture.lay” (replace the bloxCapture.lay to other maps) to train your agent on other maps in “layouts” folder.

### Part 5: Agent Report
Along with your agent, you will be required to submit a report to Moodle describing your agents’ strategy and explaining your code. 
Please include a description of your model as well as a justification for your strategy choice. 
You are expected to work independently and take reasonable steps to make sure other students can't copy or misuse your work. 
Please see: [Academic Integrity](https://www.monash.edu/students/study-support/academic-integrity)

### Part 6: Marking Rubric
#### Criteria
- Rank in the competition
- Agent strategy implementation
- Report - Description of your approach
- Report - Communication skills

#### Submission Guide
Submission to Moodle:
1. Your implementation source codes, in a single directory called "src". Zip the codes directory with the file name `last_name_student_id_pacman.zip`.
2. The report describing your approaches as a single pdf file. Name the pdf as `last_name_student_id_report_pacman.pdf`.

Submission to Contest Server:
You must make a successful submission on the server as part of your mark depending on your rank.

Submit as early as possible as you don’t know what will happen if you submit on the last day.
# FIT5222 Assignment 2

# CS Tutor | 计算机编程辅导 | Code Help | Programming Help

# WeChat: cstutorcs

# Email: tutorcs@163.com

# QQ: 749389476

# 非中介, 直接联系程序员本人
