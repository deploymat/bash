
## Frontend App [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/deploymat/bash/edit/main/DOCS/FRONTEND.md)



### Frontend APP


BUILD dependency
```bash
https://github.com/letclient/ssh ssh
```

TEST dependency
```bash
https://github.com/letclient/ssh-test ssh
```


build on remote server
```bash
./apidsl ssh.connect("IP").ssh.build("https://github.com/infrat-com/env").ssh.build("https://github.com/infrat-com/www")
```


inframonit check:
can connext to SSH?
can build or is existing the project?
is there so e different on server between version on git and filesystem on ssh?


---

deploy project
```bash
./apidsl ssh.connect("IP").ssh.clone("https://github.com/infrat-com/env").install().build().ssh.clone("https://github.com/infrat-com/www").install().build();
```