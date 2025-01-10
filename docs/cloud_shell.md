# Oracle Cloud Shell

O **Cloud Shell** é uma pequena máquina virtual executando um shell Linux, que você acessa diretamente através do navegador no **Console OCI**. Ele vem com o **OCI CLI** pré-autenticado e várias utilidades como Git, Java, Python, etc.

O **SSH** (Secure SHell) é um protocolo utilizado para login remoto seguro de um computador para outro.

## Imagem e Forma

- **Forma** é basicamente um modelo (hardware virtual) que determina o número de CPUs, a quantidade de memória e outros recursos.
- **Imagem** é o sistema operacional que roda sobre essa forma.

## Gerar Par de Chaves SSH

```bash
(shell)$ mkdir .ssh
(shell)$ cd .ssh
(shell)$ ssh-keygen -b 2048 -t rsa -f mykeyname
```

## Instalar Apache Web Server

```bash
(shell)$ sudo yum -y install httpd
(shell)$ sudo systemctl enable httpd.service
(shell)$ sudo systemctl start httpd.service
(shell)$ sudo firewall-offline-cmd --add-service=http
(shell)$ sudo firewall-offline-cmd --add-service=https
(shell)$ sudo systemctl enable firewalld
(shell)$ sudo systemctl restart firewalld
(shell)$ sudo bash -c 'echo This is my web server running on Oracle Cloud Infrastructure >> /var/www/html/index.html'
```

## Login na Instância

```bash
(shell)$ ssh -i demokey opc@<publicIPaddress>
```