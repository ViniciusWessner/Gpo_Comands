# Comandos utilizados para updates/force updates via GPO
* Todos os comandos deverão ser executados no PowerShell, algumas alteraçoes como WALPAPPER DE TELA poderão apenas funcionar somente após a reinicialização

### Reaplicar todas as políticas
        gpupdate /force
### Obtenha apenas as políticas de grupo alteradas/novas
        gpupdate
### Atualiza apenas as políticas do usuário
        gpupdate /destino:usuário
### Atualiza apenas as políticas do computador
        gpupdate /target:computador
### Algumas vezes é necessário realizarmos o logof de um determinado usuario para que seja efetivada a politica, por exemplo, após redirecionamentos de pastas ou impressoras. As alterações no AD são aplicadas apenas quando o usuário efetua login no computador, então usamos o comando abaixo.
        GPUpdate /logoff
### É necessário realizarmos a reinicialização do computador, por exemplo, quando você cria alterações no papel de parede de um grupo para isso, utilizamos o comando abaixo.
        GPUpdate /boot

<img src="https://github.com/ViniciusWessner/Gpo_Comands/blob/main/imagens/updategpo.PNG" alt="option" width="800" />