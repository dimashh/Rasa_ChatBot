## intent:greet
- hey
- hello
- hi
- good morning
- good evening
- hey there

## intent:goodbye
- bye
- goodbye
- see you around
- see you later
- talk to you later

## intent:affirm
- yes
- indeed
- of course
- that sounds good
- correct

## intent:deny
- no
- never
- I don't think so
- don't like that
- no way
- not really

## intent:mood_great
- perfect
- very good
- great
- amazing
- wonderful
- I am feeling very good
- I am great
- I'm good

## intent:mood_unhappy
- sad
- very sad
- unhappy
- bad
- very bad
- awful
- terrible
- not very good
- extremely sad
- so sad

## intent:ask_identity
- who are you
- what is your name
- how should i address you
- may i know your name
- are you a bot

<!---
  Look up from txt file
-->
## lookup:weekdays
path/to/weekdays.txt

<!---
  [value](entity name)
-->
## intent:ask_shop_open
- does the shop open on [monday](weekdays)
- does the shop open on [wednesday](weekdays)
- does the shop open on [friday](weekdays)

## lookup:countries
path/to/countries.txt

## intent:inform_country_of_origin
- i am from [malaysia](countries)
- i am from [vietnam](countries)
- i am from [thailand](countries)

<!---
  [synonym1](entity:value)
-->
## intent:ask_eaten
- what did you have for [breakfast](meal)
- what did you have for [break fast](meal:breakfast)
- what did you have for [breakfat](meal:breakfast)

## synonym:breakfast
- brekfast
- brokefast

## intent:inform_zipcode
- my zipcode is [12345](zipcode)
- my zipcode is [33456](zipcode)
- my zipcode is [94056](zipcode)

## regex:zipcode
- [0-9]{5}
