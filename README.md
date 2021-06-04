## Telegram bot "Fasteng"
After registration, new English words for learning are sent to each user at regular interval (choosen by user).
The user must answer with an emoticon back in the next 120 minutes, otherwise he will be sent a reminder that he missed the word.
Dictionary taken from [here](https://github.com/sujithps/Dictionary/blob/master/Oxford%20English%20Dictionary.txt), placed in ```/data/dictionary.txt```

### Settings
```
ruby 3.0.1
postgresql
```

### Set up
```
make install
make db-migrate
make run
```

### Usage
```make run```

Bot works in two modes:
- long polling (based on gem telegram-bot-ruby) - by default
- webhooks

To turn on webhooks-regime uncomment in bin/bot:

```
Fasteng.config.url = <your site or use ngrok>
Fasteng.config.controller = 'webhook'
```
See Makefile for additional commands
