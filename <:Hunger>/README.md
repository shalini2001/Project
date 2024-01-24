# Hunger

![image](https://github.com/shalini2001/Project/assets/66840714/f9e0223a-2afc-4133-9d23-afa598596873)
This Project aims to provide a solution to the food that is wasted in the restaurants and hotels, the excess food that is not consumed in a wedding and ends up in the garbage bins, and the loads of food that is wasted in the hostel mess. This food can be utilized to quell the hunger of the poor population of the country.

This project introduces a medium for the poor hungry person to connect to a place nearby where food is available for the donation. The donation of the food comes from the excess food in weddings, parties, hotels and restaurants which was cooked but was not consumed.
 
The whole project is divided into four major domains: 
The NLP - IVRS model. 
The database domain.
The Android application domain.
The integration of the database with the NLP model and Android application.

The Interactive Voice Response System (IVRS) model converses with the hungry person asking his/her name and address (area, city and state) in the form of speech. The user speaks the required information and through Natural Language Processing (NLP) the model converts the speech information into the text information.

On the other hand, the Android application (another part of the project) collects the information from the hotel manager, like the name and address of the hotel, and food  availability for donation.
This data is then synchronized to both the Firebase database (for authentication and infographics) and to the MongoDB database (as it supports geocoding). 

Now restaurant’s data is accessed and processed by the NLP model which first retrieves the latitude and longitude of the addresses of the restaurants from the MongoDB database. These are then converted in a geosphere circle and the minimum distance restaurant from the hungry person is obtained which also has availability of food. 

This data of the nearest restaurant (if found with the food available for donation) is then converted to a single string text format and is recited to the hungry person in the form of speech. Then the hungry person can directly go and take the food from the recommended restaurant.

This is how our project helps the poor hungry person to get free of cost and quality food from a renowned source (hotel/parties/restaurants). This also helps to minimize the food wastage and maximize the food utilization.


### App
Our android application 'Hunger' is a software that provides an easy user interface for the people with access to surplus food. It allows any restaurant manager or event manager or in fact anyone with access to excess food to update the food availability status as and when required.

An activity is the starting point for user interaction. It represents a single user interface screen. We have the following four activities with their respective functions- 
Splash Screen - The concerned people can install the app on their phones and launch it. 
Sign Up - For a first time user, they have to go to the sign up page and enter all the details like the restaurant's name, complete address, email id, contact no, username and password. 
Log In - Then they can log in using the registered username and password. If they already have an account, they can directly log in. 
Status Update - After logging in, they can update the food availability status as yes or no. They can also mention whether it's veg/non veg.

If there is a needy person nearby and they are directed to pick up food from that particular restaurant via the IVRS call system, the restaurant can pack the required amount and update the food availability status accordingly, once the pick up is successful.

The Android system helps implement the principle of least privilege.That is, by default, each app only gets access to the components it needs to accomplish its job and nothing else. This creates an extremely secure environment where a programme can't access sections of the system for which it hasn't been granted access.

Our application has been integrated with the Firebase database which grants it access to perform the CRUD operations i.e create, read, update and delete data from the database. A type of NoSQL cloud database, it can store and sync data. Data is synced in real time across all clients and is available even if the app is turned off. Data is saved in JSON format and synchronized in real time across all connected clients.

The realtime database Firebase helps manage our backend infrastructure. It enables us to -
Authentication - It helps authenticate and manage the user credentials and grant access to the 
                                       right people only.
Storage - Store and save all the relevant data given as input by the user.
Retrieval - Retrieve the user generated information as and when needed.
Realtime Updates - Get instant updates regarding food availability status.

This is how our app helps connect the ones with excess food to the ones who are in need.

### <_hunger>.pptx
A PowerPoint presentation illustrating the project's motivation and providing a detailed overview of its functionality.

### App Working.mp4
A video showcasing the operational aspects of the application.

### NLP model.mp4
A video demonstrating the functionality of the Natural Language Processing (NLP) model in voice2.py file.

### Phase-II report 19BAI10139 (1).pdf
A comprehensive report on the project, encompassing details about the technology stack used and an explanation of the motivation behind selecting such a tech stack.

### voice2.py: 

This file contains the code for the NLP processing. Below is the flowchart demonstrating the overall functionality of the code:
![image](https://github.com/shalini2001/Project/assets/66840714/619cfb1c-35bb-41d3-883d-f30cb1a97a1d)


#### Step 1: 
At first the name and location of the hungry person is asked and that is done with the help of text to speech(TTS) conversion. The person’s reply is then recognised using speech to text conversion(STT). Both TTS and STT is done with the help of pyttsx3 and speech_recognition libraries.

#### Step 2: 
After successful conversion of speech to text the text is then used for information processing. I have done this with the help of nltk and spacy libraries. With the help of nltk library a lot of essential entity models were downloaded like
‘maxent_ne_chunker’, ‘treebank’, ’‘words’, ‘punkt’, etc.

#### Step 3: 
The downloaded entity models then helped in importing another library locationtagger. This library helped in extracting the location from the entire text input so that the unnecessary words/stopwords(like ‘I’, ‘am’, ‘living’, etc.) are removed and only the keywords(like name of area and name of city) can be used for further processing.

#### Step 4: 
The keywords are then concatenated to form an address which is then passed to the MongoDB server.

#### Step 5: 
From the server when we receive the nearest restaurant name and address we store it in a variable and convert it from text to speech to tell the hungry person where it needs to go to receive food.

#### Step 6: 
In case no restaurant is found we convert the text, “No restaurant is available”' to speech to let the hungry person know that there is no restaurant near him/her that has extra food available.

#### Step 7: 
The code gave the desired output after running the python file in the command prompt/terminal.

The following libraries are used-

Pyttsx3 Library- pyttsx3 is a text-to-speech conversion library in Python. Unlike alternative libraries, it works offline and is compatible with both Python 2 and 3.

Speech Recognition- For performing Speech Recognition, there is SpeechRecognition library which is open source and several engines and APIs provide in both modes online and offline mode. 

NLTK- The Natural Language Toolkit(NLTK), is a suite of libraries and programs for symbolic and statistical natural language processing (NLP) for English written in the Python programming language. It provides a practical introduction to programming for language processing.

spaCy- It’s a free and open-source library for Natural Language Processing (NLP) in Python with a lot of in-built capabilities. It’s used for processing and analyzing data in NLP. 

Maxent_ne_chunker- The maxent_ne_chunker contains two pre-trained English named entity chunkers. It is used by the nltk.ne_chunk() function. 


Treebank- It’s a collection of syntactically annotated sentences in which the annotation is checked so that it  can serve as a training corpus for natural language parsers, as a repository for linguistic research, or as an evaluation corpus for NLP systems.

maxent_treebank_pos_tagger- NLTK is a fantastic library to support NLP. It provides a number of tagging models. The default tagging model is the maxent_treebank_pos_tagger.

Punkt- This tokenizer divides a text into a list of sentences, by using an unsupervised algorithm to build a model for abbreviation words, collocations, and words that start sentences. 

averaged_perceptron_tagger- The perceptron part-of-speech tagger implements part-of-speech tagging using the averaged, structured perceptron algorithm.

Location Tagger- Return the entity with location information. 
