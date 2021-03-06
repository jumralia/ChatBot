# ChatBot
In this Python project I am going to build a chatbot using deep learning techniques. The chatbot will be trained on the dataset which contains categories (intents), pattern and responses. I have used a special recurrent neural network (LSTM) to classify which category the user’s message belongs to and then I will give a random response from the list of responses. Let’s create a retrieval based chatbot using NLTK(Natural Language Toolkit), Keras, Python, etc.

# The Dataset
The dataset I will be using is ‘intents.json’. This is a JSON file that contains the patterns I need to find and the responses I want to return to the user.

# Steps to create a chatbot in Python from scratch:
1. Import and load the data file</br>
2. Preprocess data</br>
3. Create training and testing data</br>
4. Build the model</br>
5. Predict the response</br>
6. Run the chatbot</br>

# 1. Import and load the data file:
First, make a file name as train_chatbot.ipynb. I have imported the necessary packages for my chatbot and initialized the variables i will use in my Python project. The data file is in JSON format so I have used the json package to parse the JSON file into Python.
# 2. Preprocess data
When working with text data, I need to perform various preprocessing on the data before I make a machine learning or a deep learning model. Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words. Here, I iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. I also created a list of classes for my tags.
# 3. Create training and testing data
Now, I will create the training data in which we will provide the input and the output. Input will be the pattern and output will be the class our input pattern belongs to. But the computer doesn’t understand text so I will convert text into numbers.
# 4. Build the model
Training data ready, now I will build a deep neural network that has 3 layers. I have used the Keras sequential API for this. After training the model for 500 epochs, I have achieved 100% accuracy on my model and saved the model as ‘chatbot_model.h5’.
# 5. Predict the response (Graphical User Interface)
Now to predict the sentences and get a response from the user to let us create a new file ‘chatapp.ipynb’. 
I will load the trained model and then use a graphical user interface that will predict the response from the bot. The model will only tell the class it belongs to, so I will implement some functions which will identify the class and then retrieve a random response from the list of responses. Again I will import the necessary packages and load the ‘words.pkl’ and ‘classes.pkl’ pickle files which have been created while training my model.
# 6. Run the chatbot
To run the chatbot, use two main files; train_chatbot.ipynb and chatapp.ipynb.
First, train the model using the command in the terminal. If you use terminal save file in .py format and run following command: python train_chatbot.py</br>
If you don’t see any error during training, you have successfully created the model. </br>
Then to run the app, run the second file: python chatapp.py</br>
The program will open up a GUI window within a few seconds. With the GUI you can easily chat with the bot.
