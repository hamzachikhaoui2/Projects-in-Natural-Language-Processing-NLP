## General information :

### The Final Submission folder is divided into 5 main compartments :

1) The PDF, which corresponds to the final report written on overleaf, which contains most of the information about our final project.

2) The COMBINED GIFs subfolder, which contains gifs showing the behaviour of the robot for a given command in natural language parsed using our Rule Based Method (depicted on the left), and parsed using the LLM based method (depicted on the right).

3) The first_pkg subfolder which contains all the code necessary to run the simulation in the virtual environment.

4) The full outputs, which corresponds to the full outputs of the RB Method and the LLM based method for the full list of 15 prompts

5) The Jupyter Notebooks Code which contains 2 codes : The first one corresponds to a summed up version presenting the final code for each method (i.e. FinalCodeSubmissionCOMP550), and a code that shares all the experiments we conducted over the entire course of the project (i.e. AllIterationsOfCode(fullInvestigation)


## Install the following packages to ensure the project works correctly:

1. **Transformers**  
   ```bash
   pip install transformers
   ```

2. **Torch**  
   ```bash
   pip install torch
   ```

3. **OpenAI** (version 0.28)  
   ```bash
   pip install openai==0.28
   ```

4. **Sentence Transformers**  
   ```bash
   pip install sentence-transformers
   ```

5. **Scikit-learn**  
   ```bash
   pip install scikit-learn
   ```

6. **Pandas**  
   ```bash
   pip install pandas
   ```

7. **SpaCy**  
   ```bash
   pip install spacy
   ```

8. **NLTK**  
   ```bash
   pip install nltk
   ```


###########################################################################################



README: Instructions for Executing turtle_actions.launch in first_pkg

Follow the steps below to set up and run the launch file turtle_actions.launch in the first_pkg package:

## Prerequisites
1. Operating System:
	Use Ubuntu 20.04.
	
2. Install ROS Noetic:
	Follow the official ROS Noetic installation guide: https://wiki.ros.org/noetic/Installation/Ubuntu
	
## Setting Up the Workspace and Package
1. Create a Catkin Workspace:
	* Open a terminal and run the following commands:
		>> mkdir -p ~/catkin_ws/src
		>> cd ~/catkin_ws/
		>> catkin_make
		
2. Include the first_pkg Package in Your Workspace:
	* Include the first_pkg package into the src directory of the catkin_ws workspace

3. Build the Workspace:
	>> cd ~/catkin_ws
	>> catkin_make

4. Source the Workspace:
	* Source the workspace in the current terminal session:
		>> source ~/catkin_ws/devel/setup.bash
		
## Running the Launch File
1. Open a Terminal:
	* Ensure your terminal is set up with ROS and your workspace sourced.

2. Run the Launch File:
	* Execute the following commands each on a different terminal:
		>> roscore
		>> rosrun turtlesim turtlesim_node
		>> roslaunch first_pkg turtle_actions.launch
