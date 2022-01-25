# Comandos para updates/force updates GPO
* Todos os comandos deverão ser executados no PowerShell, algumas alteraçoes como WALPAPPER DE TELA poderão apenas funcionar somente após a reinicialização

### Reaplicar todas as políticas
        gpupdate /force
### Obtenha apenas as políticas de grupo alteradas/novas
        gpupdate
### Atualiza apenas as políticas de um único usuário
        gpupdate /destino:usuário
### Atualiza apenas as políticas de um único computador
        gpupdate /target:computador
### Atualizar politicas fazendo LOGOFF do usuário
* Algumas vezes é necessário realizarmos o logof de um determinado usuario para que seja efetivada a politica, por exemplo, após redirecionamentos de pastas ou impressoras. As alterações no AD são aplicadas apenas quando o usuário efetua login no computador, então usamos o comando abaixo.
        GPUpdate /logoff
### Atualizar reiniciando a maquina
* É necessário realizarmos a reinicialização do computador, por exemplo, quando você cria alterações no papel de parede de um grupo para isso, utilizamos o comando abaixo.
        GPUpdate /boot
### Atualizar GPO por interface
* Você pode iniciar uma atualização de política de grupo em uma UO inteira com o Console de Gerenciamento de Política de Grupo. Tem que ser uma UO com apenas objetos de computador, então você não pode usar o método em uma UO de usuário. Basta clicar com o botão direito do mouse na UO onde você alterou uma política e clicar em Group Policy Update
Isso atualizará as políticas do usuário e do computador em todos os computadores da unidade organizacional especificada. O bom é que ele irá confirmar e mostrar quantos computadores serão atualizados.
<br>
<img src="https://github.com/ViniciusWessner/Gpo_Comands/blob/main/imagens/updategpo.PNG" alt="option" width="500" align="center" />

<img src="https://github.com/ViniciusWessner/Gpo_Comands/blob/main/imagens/aposupdate.PNG" alt="option" width="500" align="center" />