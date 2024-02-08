## Mailtrap - test SMTP server

https://github.com/dbck/docker-mailtrap

Roundcube web mail on http://localhost:9080/


## API access

Get messages:
http://localhost:9080/api/inbox

Flush all messages
http://localhost:9080/api/inbox?flush=true

## Send a test mail

```
docker-compose exec mailtrap /bin/bash
telnet mailtrap 25
ehlo example.com
mail from: me@example.com
rcpt to: you@example.com
data
Subject: Hello from me
Hello You,

This is a test.

Cheers,
Me
.
quit
exit
```