# NMAP

Nesse repositório vou abordar  alguns comandos do Nmap.
O Nmap é uma ferraemnta muito valiosa para um ataque, pois a mesma possibilita você de conhecer o terreno que você está atacando, quais os sistemas operacionais de cada Host e quais vulnerabilidades os mesmos possuem.
Depois de "varrer" a infraestrutura do defensor você tem que arquitetar quais serão os alvos, e quais os ataques que podem ser desenvolvidos para esses alvos. 


fping -g 192.168.0.100/24 2>/dev/null | grep "is alive" 
Esse comando faz uma verificação de quais hosts estão ativos na rede 
puxando do 192.168.0.1 ao 192.168.0.254 e os que estiverem ativos ele exibirar uma mensagem "is alive" (está vivo).

nmap -sV -p 21,22,23,80,139,445, 192.168.0.1 
Esse comando descobre qual é o fabricante do dispositivo e quais portas estão abertas e seus respectivos serviços. 

nmap -Pn 192.168.0.1 -top-ports=100
Esse comando identifca quais as principais portas baseada nas 100 mais utilizadas e vai retornar se estão abertas ou fechadas. 

nmap -sV -p 21,22,23,80,139,445, -O 192.168.0.1 
Esse comando serve para identificar o SO do host e ajuda identificar quais portas estão abertas nele também. 

nmap --script "vuln" -p 21,22,23,80,139,445  192.168.0.1
Nesse comando será executado um script para encontrar uma vulnerabilidade para aquele host, a vulnerabilidade sera exibida como CVE, normalmente é composta de oito digitos separados.
