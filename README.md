Notifier
===========

Simple WebSocket notifications through RabbitMQ

## Usage

Run notifier:
```
go run *.go --addr=:5000 --debug=true --ssl=false
```

Go to [notification page](http://localhost:5000/) and enter your ID

Send notification through RabbitMQ, for example:
```
pip install universalbus
```
and then
```
from universalbus import EventSender
sender = EventSender('guest', 'guest', 'localhost', '/', exchange='notifications')
sender.push_text('user.15', 'notification example')  # instead 15, enter your ID
```


