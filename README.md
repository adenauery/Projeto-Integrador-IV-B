# Projeto-Integrador-IV-B

**Professores Responsáveis**

Emails para contato:
* Alexandra Zimpeck - alexandra.zimpeck at ucpel.edu.br 
* Adenauer Yamin - adenauer.yamin at ucpel.edu.br

## Procedimento Exigido para Entrega Parcial

### Introdução ao LDAP, material de auxílio elaborado por bolsista do G3PD
* [Material Organizado por Ronaldo Cunha - G3PD](http://olaria.ucpel.edu.br/rcunha/)

### Instalação de uma Máquina Virtual
* Procedimentos utilizados
* Ambiente de virtualização
* Distribuição empregada para criação da Máquina Virtual
* Configuração empregada na Máquina Virtual

## Procedimento Exigido para a Entrega Final

### Instalando o Servidor OpenLDAP e uma Interface Web de Gerência
* [Tutorial em Portugues para instalar o OpenLDAP e a Interface de Gerência phpLDAPadmin](https://www.zentica-global.com/pt/zentica-blog/ver/como-instalar-openldap-e-phpldapadmin-no-ubuntu-server-20.04-60737ebe0b7a3)
* [Tutorial em Inglês para Instalação do OpenLDAP e a Interface de Gerência phpLDAPadmin](https://idroot.us/install-openldap-ubuntu-20-04/)

**OBS: Quem instalar no Ubuntu Server, ou outra distro no modo servidor, deverá utilizar outro equipamento (ou máquina virtual) para fazer acesso a interface Web.**

* [Tutorial em Vídeo sobre a Instalação do OpenLDAP](https://www.youtube.com/watch?v=JaZuLHDQkSU) - **Excelente sugestão do colega Pablo Lopes**

#### Opção de Interface para Gerência Web do OpenLDAP
* [LDAP Account Manager](https://computingforgeeks.com/install-and-configure-ldap-account-manager-on-ubuntu/)

## Servidor de Teste:
* URL: http://152.70.223.181/phpldapadmin/
* Username: cn=admin,dc=projeto,dc=integrador,dc=br
* Password: **enviada por email**


## Informações Adicionais Cujos Procedimentos Não Serão Cobrados nas Entregas

### Instalando o OpenLDAP - Cliente
* [Configure Linux Clients To Authenticate Using OpenLDAP](https://www.unixmen.com/configure-linux-clients-to-authenticate-using-openldap/)

### Utilizando Equipamentos em Nuvem
* [Plataforma da Oracle](https://www.oracle.com/br/index.html)
* [O que é gratuito na Plataforma da Oracle](https://www.oracle.com/br/cloud/free/#always-free)
* [Exemplo de como abrir portas em uma VM na nuvem da Oracle](https://docs.oracle.com/en/learn/lab_compute_instance/index.html#introduction)
#### Procedimentos após a ativação da Máquina Virtual
* Fazer Download da Chave Privada
* Comando trocar as permissões da Chave Privada para 400 
  * chmod 400 <chave privada>
* comando para acessar a Máquina Virtual:
  * ssh -i /Users/adenauer/Desktop/Chaves-Oracle/<chave privada> ubuntu@152.70.223.181 -p 22
* liberar o acesso por password, utilize o tutorial abaixo:
  * https://www.simplified.guide/ssh/disable-password-authentication
* Liberando acesso a porta 80 (HTTP) em Instancias (VMs) do Oracle Cloud:
 * Ajustar na Virtual Cloud Networks o acesso a porta 80
 * Liberar o acesso a porta 80 na Firewal [fonte](https://stackoverflow.com/questions/54794217/opening-port-80-on-oracle-cloud-infrastructure-compute-node)
   * sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
   * sudo netfilter-persistent save
   * sudo systemctl restart apache2
 
### Provedores de IAAS em Cloud
* https://www.cloudatcost.com/
* https://www.oracle.com/
 
### LDAP em Nuvem
* [jumpcloud](https://jumpcloud.com/)
