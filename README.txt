README for Walking Robot and Reinforcement Learning Model

Copyright (c) November 2024 Amin Tadayyoni, Behnam Miripour Fard, Ali Jamali
 cite this article: "Robust walking motion generation for biped robots... 
  using manipulability based- reinforcement learning"
For any questions, email us at: bmf@guilan.ac.ir or amintadayyonihsu@gmail.com


This documentation provides an overview of the four main components in this repository:

1. Script: "model_test_A_T"
   - This script details the license and citation requirements for the use of the provided code and model.
   - It must be executed prior to using other scripts or models to ensure compliance with these conditions.

2. File: "Robot & RL Parameters"
   - Within this file, the "robotParametersRL_Test" script specifies the robot's physical attributes and key model parameters.
   - It enables users to introduce length and weight uncertainties to the robot model. The script includes details on how these uncertainties can be applied.

3. File: "Environment_RL&Robot_model"
   - This file contains two Simulink models:
       - "walkingRobotRL3D" is the primary robot and system environment model as referenced in the initial source.
       - "walkingRobotRL3D__Test_with_51_obs" represents an enhanced model based on the current article. In this updated environment, users can add disturbances described in the article, observe test outcomes, adjust observation space dimensions, and modify simulation termination conditions relative to the original model.

4. File: "Agents"
   - This file includes trained agents used in both the initial source and the article referenced in the license section. Each agent's training results are also provided. A breakdown of the agents is as follows:
       - Trained Agents from the Article:
           1. trainedAgent_RH: Agent focused on reward hacking, as discussed in the article.
           2. Agent5458_J: Agent trained with the manipulability parameter.
           3. Agent6740_without_J: Agent trained without the manipulability parameter.
       - Agent from the Initial Reference:
           - trainedAgent_3D_11_04_2019_0102: Agent trained following the original reference.
   - Agents trainedAgent_RH and trainedAgent_3D_11_04_2019_0102 are compatible with "walkingRobotRL3D."
   - Agents Agent5458_J and Agent6740_without_J should be run with the enhanced model, "walkingRobotRL3D__Test_with_51_obs."

Requirements and Usage Guide:

Requirements:
   - This code has been tested on MATLAB version 2023a. It is recommended to use MATLAB 2023a or later for optimal compatibility.

Usage Steps:
   1. Run the "model_test_A_T" script to initialize licensing requirements.
   2. Select the appropriate model ("walkingRobotRL3D" or "walkingRobotRL3D__Test_with_51_obs") based on the desired agent.
   3. Open one of the agent files from "Agents" according to the model choice.
   4. Input the agent name into the Simulink model’s RL Block as "saved_agent" or "agent" and run the model.
      - The simulation results and robot modeling in the Multi-Body environment will then be viewable.
