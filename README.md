Welcome to NatLTL Tool Guide:

This guide teaches the user how to use NatLTL tool. Download and extract the project from the zip file and follow the steps carefully to execute them correctly.

HOW TO SUCCESSFULLY RUN YOUR CODE
Preliminary Step: DOWNLOAD ALL NECESSARY LIBRARIES

The user should extract the main folder and execute the project in a Python environment that supports some existing libraries used in it, such as NumPy, BinaryTree, etc. Download them if they are not already installed.

1.1: INPUT FILES

Firstly, to start, you will need two .txt files representing both the model and the LTL formula. You can find both of them inside the TESTING folder as exampleModel(n).txt and exampleFormula(n).txt.

We strongly recommend you to begin with these files to understand the whole process, and then customize them as you desire.

To successfully run the entire project, you will need to modify the following paths:

model = ''C:\\Users\\utente\\Desktop\\Testing\\LogisticRobot.txt'
formula = ''C:\\Users\\utente\\Desktop\\Testing\\formulaLTL.txt'
result = ''C:\\Users\\utente\\Desktop\\Testing\\Result.txt'

Representing respectively the input model, the LTL formula intended in syntax, a result file where save the results obtained.

These can be found inside the main files that are intended as isNotNash.py and sureWin.py and must be replaced with the absolute paths of the files you download from the TESTING folder to your local computer.

Note: Only exampleModel(n).txt and exampleFormula(n).txt need to be nonempty at the beginning; the other files can be empty!!

1.2: PROGRAM EXECUTION

If you followed the instructions in section 1.1, you will be able to launch the program by running isNotNash.py file or sureWin.py file (based on your preferences). 

HOW TO MODIFY INPUT FILES
2.1: FORMULA ALTERATION

To modify a formula, follow the LTL syntax rules. You can choose between X, G, F, and U temporal operators to construct SIMPLE LTL formulas with a single temporal operator.

2.2: MODEL ALTERATION

To modify the model, if you want to add a state, you have to add a new row and a new column to the transition matrix (Transition), placing the idle element in the new diagonal position. Then you have to add an extra row to the label matrix (Labelling), and also add the new state name in the name_state position.

2.3: TOTAL AGENTS ALTERATION

It is also possible (inside the exampleModel file) to define the total number of agents in the model. To add an agent, increase this number by one and add a unique set of actions for the new agent. These actions should also be reported in the Transition Matrix at the agent's new position. For example, if you add an extra agent and now have four agents in the coalition, it is mandatory to adjust all the matrix elements (apart from 0s) by adding a fourth character that matches one of the new agent's actions. For instance, the initial element ADF would become ADFZ, earning a new string character that correspond to the new agent action.

Conversely, you can reduce the number of agents by subtracting from the total number of agents and removing the corresponding element string characters from the Transition Matrix that match the removed agent's actions.

2.4: ATOMIC PROPOSITION ALTERATION

To add a new atomic proposition, modify the atomic propositions row inside the exampleModel file. Additionally, add a new column to the Labelling Matrix, placing 1's in the states where you want the proposition to hold (for example, for the first row (s1), your column will have a 1) and 0 elsewhere.

On the other hand, you can reduce the number of atomic propositions by removing it from atomic_propositions and deleting its corresponding column in the Labelling Matrix.

Thanks!
