## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## story 01
* inform
  - utter_ask_location

## story 04
* inform
  - action_weather

## Generated Story -4510910781578829675
* greet
    - utter_greet
* ask_identity
    - utter_cheer_up
* ask_shop_open{"weekdays": "monday"}
    - utter_happy
