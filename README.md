# Smart-Assistant

Build a chatbot

install the latest Anaconda software on your computer since we will be setting up our virtual environment using it.

Open up the terminal window in your RPi using VNC viewer run the following command.

     conda create --name botenv python=3.7
     conda activate botenv
This command activates the virtual environment where we will use to run our chatbot. Now using PIP run the command below to install Rasa.

     pip install rasa-x --extra-index-url https://pypi.rasa.com/simple
This will install the Rasa library on your RPi.

Rasa uses different components to recognize intents and entities, and the majority of them have additional dependencies. For now, we will make use of the spacy library which is a popular option.

Run the following commands on your terminal.

     pip install rasa[spacy]
     python -m spacy download en_core_web_md
     python -m spacy link en_core_web_md en
     pip install rasa_core
Furthermore, if you want to install all the dependencies that you might ever work with and do not mind it lying around in your directories, then run the following command

     pip install -r alt_requirements/requirements_full.txt
Now that all the requirements are installed, let us go ahead with our project.

Let us name our bot as Chatty. We will create a base project directory for both the training files and data files.

     mkdir chatty
     cd chatty
     mkdir data
     cd data
     touch nlu.md

The folder 'data' will contain our data files and we will save our training file in data directory as nlu.md

Touch is a command used in Linux to create a file without any content in them. The file created using touch command is empty. This command is mainly used when the user does not have any data to store at the time of file creation.
