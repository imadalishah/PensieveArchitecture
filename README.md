# Neural Adaptive Video Streaming with Pensieve
Implementation of [original](web.mit.edu/pensieve/) paper : Neural Adaptive Video Streaming with Pensieve (SIGCOMM '17)

**Original Contributors:**
[Hongzi Mao](https://github.com/hongzimao/pensieve)
[Ahmad ALHILAL](https://github.com/ahmad-hl/pensieve-py38)


# **Implementation of Original Pensieve Architecture in Python3+ and on Google Colab**

Steps are written below for better understanding of the notebook working. However, [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1My3p3JtomCWsuwSGKn4wbSk1y4buWd7E?usp=share_link) is available to be run directly for ease.

**To run the Pensieve Architecture and reproduce the results of the papers on Google Colab, follow these steps:**
1. Open a new notebook on Google Colab.
2. Set the runtime type to Python 3.8.
3. Install the required dependencies using the following command:
   `!pip install tensorflow tflearn matplotlib selenium`
4. Clone the Pensieve repository from My [GoogleDrive](https:////drive.google.com/drive/folders/1LAkFiMLk85r_rfcbf_mBSRyR1tmvBAcX?usp=share_link) to your drive 
5. Change the working directory to the Pensieve repository:
   `%cd /content/drive/MyDrive/pensieve`
6. Put the training data in the 'sim/cooked_traces' folder and testing data in the 'sim/cooked_test_traces' folder.
7. Run the '`!python sim/get_video_sizes.py`'
8. Train a new model by running the '`!python sim/multi_agent.py`'
9. Monitor the testing curve of rewards, entropy, and TD loss by launching Tensorboard from the terminal: by running '`!tensorboard --logdir=sim/`'
10. To test the trained model in a simulated environment, copy over the model to test/models and modify the NN_MODEL field in test/rl_no_training.py. Then, run the '`!python test/get_video_sizes.py`'
11. Run the '`!python test/rl_no_training.py`' script
12. To run experiments over Mahimahi emulated network, copy over the trained model to rl_server/results and modify the NN_MODEL field in rl_server/rl_server_no_training.py. Then, run the '`!python run_exp/run_all_traces.py`' script
13. To run real-world experiments, first set up a server (setup.py automatically installs an Apache server and put needed files in /var/www/html). Then, copy over the trained model to rl_server/results and modify the NN_MODEL field in rl_server/rl_server_no_training.py. Next, modify the url field in real_exp/run_video.py to the server URL. Finally, run the '`!python real_exp/run_exp.py`' script
14. To view the training and cross-validation (testing) curve using Tensorboard, run '`!tensorboard --logdir=sim/`'
15. The TD loss and total reward of multi_agent.py can be monitored in Tensorboard by selecting the relevant metrics.


# **Contact**

[![LinkedIn](https://user-images.githubusercontent.com/57298558/231293935-ead7992d-43a1-4de7-a023-3800fdecd331.png)](https://www.linkedin.com/in/imadalishah)
[![Twitter](https://user-images.githubusercontent.com/57298558/231293638-7be4782a-6851-4049-969e-0bd0ce067276.png)](https://www.twitter.com/imadalishah)
[![Github](https://user-images.githubusercontent.com/57298558/231293745-ae272207-5087-4ea6-a3ee-184fccc8a492.png)](https://www.github.com/imadalishah)

