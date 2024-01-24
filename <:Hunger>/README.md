Hunger

App: The code employed in developing the application.

<_hunger>.pptx: A PowerPoint presentation illustrating the project's motivation and providing a detailed overview of its functionality.

App Working.mp4: A video showcasing the operational aspects of the application.

NLP model.mp4: A video demonstrating the functionality of the Natural Language Processing (NLP) model in voice2.py file.

Phase-II report 19BAI10139 (1).pdf: A comprehensive report on the project, encompassing details about the technology stack used and an explanation of the motivation behind selecting such a tech stack.

voice2.py: The following steps demonstrates the code:

● Step 1: At first the name and location of the hungry person is asked and that is done with the help of text to speech(TTS) conversion. The person’s reply is then recognised using speech to text conversion(STT). Both TTS and STT is done with the help of pyttsx3 and speech_recognition libraries.

● Step 2: After successful conversion of speech to text the text is then used for information processing. I have done this with the help of nltk and spacy libraries. With the help of nltk library a lot of essential entity models were downloaded like
‘maxent_ne_chunker’, ‘treebank’, ’‘words’, ‘punkt’, etc.

● Step 3: The downloaded entity models then helped in importing another library locationtagger. This library helped in extracting the location from the entire text input so that the unnecessary words/stopwords(like ‘I’, ‘am’, ‘living’, etc.) are removed and only the keywords(like name of area and name of city) can be used for further processing.

● Step 4: The keywords are then concatenated to form an address which is then passed to the MongoDB server.

● Step 5: From the server when we receive the nearest restaurant name and address we store it in a variable and convert it from text to speech to tell the hungry person where it needs to go to receive food.

● Step 6: In case no restaurant is found we convert the text, “No restaurant is available”' to speech to let the hungry person know that there is no restaurant near him/her that has extra food available.

● Step 7: The code gave the desired output after running the python file in the command prompt/terminal.

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
