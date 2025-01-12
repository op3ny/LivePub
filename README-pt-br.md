Seção 1 - Para o usuário!

# Sobre

Olá! Bem-vindo ao Github do LivePub. O LivePub é um projeto Open Source que irá ajudá-lo a hospedar sua própria transmissão ao vivo. Com um painel amigável e uma forma simples de instalar! Então espero que vocês gostem e vamos começar!

# Imagens

[Clique aqui para acessar](https://github.com/op3ny/LivePub/tree/main?tab=readme-ov-file#images)

# Vamos começar!

Ok, antes de começar, você precisa tentar usar nossa demonstração do LivePub (Você pode acessar por: Num existe mais, boa sorte aê... ).

Este site será executado localmente no seu computador e explicarei como.

# Requisitos:

Ram: 2gb

CPU: (Provavelmente funcionará com sua CPU)

Sistema operacional: Ubuntu 22.04 LTS (recomendo usar Ubuntu 22.04 LTS ou Ubuntu 20.04 LTS)

Aplicativos: ffmpeg, python3, python3-pip, nginx (o script fará isso por você!)


# O código!

Primeiro você precisará baixar nosso script
Código:
```
sudo su
```
```
apt update && apt upgrade -y
```
```
apt install wget curl -y
```
```
wget ​​https://raw.githubusercontent.com/op3ny/LivePub/main/script.sh
```
VERSÃO EM PORTUGUÊS ------^

```
wget https://raw.githubusercontent.com/op3ny/LivePub/main/script2.sh
```
VERSÃO EM INGLES ---------^
```
chmod 777 script.sh
```
```
./script.sh
```

Ao final você precisa reiniciar sua máquina, com este comando:
```
reboot
```

# Você está usando isso em outro pc (Sem ser localhost)

Se você não está usando o LivePub em seu próprio pc, você precisa alterar:  

/var/www/html/backend/render.py - Line: 104
Change localhost to your pc's public ip.

/var/www/html/backend/create-channel.html - Line 9
Change 127.0.0.1 to your pc's public ip.

/var/www/html/backend/delete-channel.html - Line 10
Change 127.0.0.1 to your pc's public ip.

E você precisa abrir as portas:


3398 - Delete channel service
3389 - Create channel service
1935 - RTMP port
80 - HTTP port

# Você terá que alterar sempre!

/var/www/html/backend/render.py - Line 68
Change livepub.ddns.net to your pc'a public ip.

You need to open the ports:

3398 - Delete channel service  /  
3389 - Create channel service  /  
1935 - RTMP port  /  
80 - HTTP port  /  


# Novos comandos!

No seu sistema, você terá três novos comandos (funciona apenas no root)
```
livepub-start
```
Inicie o LivePub
```
livepub-stop
```
Pare o LivePub
