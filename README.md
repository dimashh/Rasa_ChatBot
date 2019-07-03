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
