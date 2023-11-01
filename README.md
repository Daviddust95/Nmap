# Pentesting com Nmap - Guia Educacional

Este repositório é criado estritamente para fins educacionais.

## Introdução
<justify>
Nesse repositório vou abordar alguns comandos do Nmap. O Nmap é uma ferramenta muito valiosa para um ataque, pois a mesma possibilita você de conhecer o terreno que você está atacando, quais os sistemas operacionais de cada Host e quais vulnerabilidades os mesmos possuem. Depois de "varrer" a infraestrutura do defensor você tem que arquitetar quais serão os alvos, e quais os ataques que podem ser desenvolvidos para esses alvos.
</justify>

# 1. Instalação do Nmap
## No Ubuntu e sistemas baseados no Debian:

**Abra o terminal no seu sistema Ubuntu ou qualquer sistema baseado no Debian.**

2. Atualize o cache de pacotes com o comando:
- ```bash
   sudo apt update
3. Instale o Nmap usando o comando:
- ```bash
  sudo apt install nmap
4. Para verificar se o Nmap foi instalado, digite:
- ```bash
  nmap --version

## No CentOS, Fedora e sistemas baseados no Red Hat:
### 1. Abra o terminal no seu sistema CentOS, Fedora ou qualquer sistema baseado no Red Hat.

### 2. Use o gerenciador de pacotes dnf ou yum para instalar o Nmap. Para sistemas mais recentes que usam dnf, execute o seguinte comando:
- ```bash
  sudo dnf install nmap
## Para sistemas mais antigos que usam yum, execute o seguinte comando:
- ```bash
  sudo yum install nmap
## No openSUSE:
### 1. Abra o terminal no seu sistema openSUSE.

### 2. Use o comando zypper para instalar o Nmap:
## Comandos Básicos do Nmap
- ```bash
  sudo zypper install nmap

## No Arch Linux:
### 1. Abra o terminal no seu sistema Arch Linux.

### 2. Use o pacman para instalar o Nmap:
- ```bash
  sudo pacman -S nmap


## 2. Verificação de Hosts Ativos

**Para identificar hosts ativos em uma rede:**

**Este comando verificará quais hosts estão ativos na rede no intervalo de 192.168.0.1 a 192.168.0.254, e os que estiverem ativos ele exibirar uma mensagem "is alive" (está vivo).**
-  ```bash
    fping -g 192.168.0.100/24 2>/dev/null | grep "is alive"

**Esse comando descobre qual é o fabricante do dispositivo e quais portas estão abertas e seus respectivos serviços.**
- ```bash
    nmap -sV -p 21,22,23,80,139,445, 192.168.0.1

**Esse comando escaneia a faixa de portas em um ip, dns, ou url que você determinar.**
- ```bash
    nmap -p 0-65535

**Esse comando identifca quais as principais portas baseada nas 100 mais utilizadas e vai retornar se estão abertas ou fechadas.**
- ```bash
    nmap -Pn 192.168.0.1 -top-ports=100

**Esse comando serve para identificar o SO do host e ajuda identificar quais portas estão abertas nele também.**
- ```bash
    nmap -sV -p 21,22,23,80,139,445, -O 192.168.0.1

**Nesse comando será executado um script para encontrar uma vulnerabilidade para aquele host, a vulnerabilidade sera exibida como CVE, normalmente é composta de oito digitos separados.**
- ```bash
    nmap --script "vuln" -p 21,22,23,80,139,445 192.168.0.1

## Aviso
<justify>
Este repositório é apenas para fins educacionais. Não promovemos atividades ilegais ou antiéticas. Certifique-se de obedecer às leis locais e diretrizes éticas ao usar o Nmap e outras ferramentas de segurança.
Lembre-se de usar esses comandos de maneira responsável e ética. A segurança cibernética é um campo sério e deve ser usada para fins legítimos, como testar a segurança de seus próprios sistemas ou com permissão legal.
Sinta-se à vontade para explorar os comandos acima e aprofundar seu conhecimento em testes de penetração com o Nmap. Lembre-se de usá-los de maneira responsável e respeitando a privacidade e a segurança de terceiros.
<justify>

## Contato
Se você tiver alguma dúvida, comentário ou feedback, sinta-se à vontade para entrar em contato:

- **Email:** alissondaviddev@gmail.com
- **LinkedIn:** [alisson-melo95](https://www.linkedin.com/in/alisson-melo95/) 
- **Site Pessoal:** [Portifólio](https://alissondev.tech)
- **GitHub:** [@Daviddust95](https://github.com/Daviddust95)

