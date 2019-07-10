# Rasa_ChatBot

Simple chat bot on rasa for classifying intents and recognising entities.
* *Rasa uses the concept of intents to describe how user messages should be categorized.*
* *Entity are different pieces of relevant information that are extracted from user messages such as date and address.*

## To train the nlu model, run:
```rasa train nlu```

## To test the model, run:
```rasa shell nlu```

## To test a specific nlu model, run the following command with appropriate version from /models
```rasa shell -m models/nlu<version.tar.gz>```

## Run nlu server:
```rasa run --enable-api -m models/nlu<version.tar.gz>```

## In a new terminal run:
* ```curl localhost:5005/model/parse -d '{"text":"hello"}'```
* You should be to obtain a json result indicating the intent and confidence level
* ```{"intent":{"name":"greet","confidence":0.9770460725},"entities":[],"intent_ranking":[{"name":"greet","confidence":0.9770460725},{"name":"mood_unhappy","confidence":0.0257926807},{"name":"ask_identity","confidence":0.0009481288},{"name":"mood_great","confidence":0.0},{"name":"inform_identity","confidence":0.0},{"name":"goodbye","confidence":0.0}],"text":"hello"}```

| Command                     | Effect                                                                                    |   
| :--------------------------:|:-----------------------------------------------------------------------------------------:|
| ```rasa init```             | Creates a new project with example training data, actions, and config files.              |
| ```rasa train```            | Trains a model using your NLU data and stories, saves trained model in ./models.          |   
| ```rasa interactive```      | Starts an interactive learning session to create new training data by chatting.           |
| ```rasa shell```            | Loads your trained model and lets you talk to your assistant on the command line.         |
| ```rasa run```              | Starts a Rasa server with your trained model. See the Running the Server docs for details.|
| ```rasa run actions```      | Starts an action server using the Rasa SDK.                                               |
| ```rasa visualize```        | Visualizes stories.                                                                       |
| ```rasa test```             | Tests a trained Rasa model using your test NLU data and stories.                          |
| ```rasa data split nlu```   | Performs a split of your NLU data according to the specified percentages.                 |
| ```rasa data convert nlu``` | Converts NLU training data between different formats.                                     |
| ```rasa x```	              | Launch Rasa X locally.                                                                    |
| ```rasa -h```	              | Shows all available commands.                                                             |
