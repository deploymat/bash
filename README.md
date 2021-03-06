

![logo.deploymat.com](https://logo.deploymat.com/1/cover.png)

## About [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/deploymat/bash/edit/main/DOCS/ABOUT.md)



## deploy app

letclient
+ ssh
+ http

letapi
+ github
+ gitlab

browser bot
+ botreck puppeteer


## DeployMat [<span style='font-size:20px;'>&#x270D;</span>](https://github.com/deploymat/bash/edit/main/DOCS/DEPLOY.md)


### Prepare Plesk Server

dependency
```bash
https://github.com/botreck/plesk plesk
```

based on botreck templates
```bash
./apidsl plesk.add_plesk_subscription("softreck.dev").
```


### prepare infrastructure on github

dependency
```bash
https://github.com/letapi/github.com github
```

code
```bash
./apidsl github.add_project("infrat/www").github.add_domain_to_project("infrat.com").github.set_template("infrat.com","black")
```



### prepare infrastructure on Registrar

dependency
```bash
https://github.com/botreck/strato.de strato.de
```

based on botreck templates
```bash
./apidsl strato.domain("softreck.dev").strato.dns_from_file("digitalocean.txt")
```

```bash
./apidsl strato.domain("softreck.dev").strato.dns_from_file("digitalocean.txt")
./apidsl load("digitalocean.txt").strato.dns()
```

---

```bash
./apidsl strato.add_domain("infrat/www").github.add_domain_to_project("infrat.com").github.set_template("infrat.com","black")
./apidsl deployapk.add_plesk_subscription("softreck.dev")
```

```bash
./apidsl strato.add_domain("infrat/www").github.add_domain_to_project("infrat.com").github.set_template("infrat.com","black")
./apidsl deployapk.add_plesk_subscription("softreck.dev")
```


deployapk.registrar("strato.de")
load("digitalocean.txt").deployapk.nameservers()

```

deployapk.registrar("aftermarket")

```
deployapk.clone("https://github.com/infrat-com/env")
deployapk.install()
deployapk.build()
deployapk.clone("https://github.com/infrat-com/www")
deployapk.install()
deployapk.build()
deployapk.test()
deployapk.domain_nameservers("")
deployapk.domain_provider("")
deployapk.domain_registrar("")

deployapk.domomain_ns("")
deployapk.cloudflareNs("")
deployapk.plesk("softreck.dev")
deployapk.cloudflare("softreck.dev")
```

```
deployapk.github("infrat-com/www")
.split("/n")
.http()
.xpath("title")
.appendToFile("titles.txt")
```

Backend APP
```js
deployapk.git("")
deployapk.ns("")
deployapk.plesk("softreck.dev")
deployapk.cloudflare("softreck.dev")
.split("/n")
.http()
.xpath("title")
.appendToFile("titles.txt")
```

API integration
```js
deployapk.git("")
deployapk.ns("")
deployapk.plesk("softreck.dev")
deployapk.cloudflare("softreck.dev")
.split("/n")
.http()
.xpath("title")
.appendToFile("titles.txt")
```

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


# Tags

+ scripts
+ language

---

+ [edit](https://github.com/deploymat/bash/edit/main/README.md)
+ [deploymat/bash](https://github.com/deploymat/bash)
