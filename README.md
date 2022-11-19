# Projeto-Integrador-IV-B

**Professores Responsáveis**
* [Victoria Souto](mailto:victoria.souto@ucpel.edu.br)
* [Adenauer Yamin](mailto:adenauer.yamin@ucpel.edu.br)

## Procedimento Exigido para Entrega Parcial

#### Conceitos referentes ao LDAP e Instalação das Máquinas Virtuais

* [Material Organizado pela Profa. Victoria Souto](https://drive.google.com/drive/folders/151NHlJMR3eQ3VoWck3obb7J0mXuJMJrF)


## Procedimento Exigido para a Entrega Final

#### Instalando o Servidor OpenLDAP e uma Interface Web de Gerência
* [Tutorial em Portugues para instalar o OpenLDAP e a Interface de Gerência phpLDAPadmin](https://www.zentica-global.com/pt/zentica-blog/ver/como-instalar-openldap-e-phpldapadmin-no-ubuntu-server-20.04-60737ebe0b7a3)
* [Tutorial em Inglês para Instalação do OpenLDAP e a Interface de Gerência phpLDAPadmin](https://computingforgeeks.com/install-and-configure-openldap-phpldapadmin-on-ubuntu/)

**OBS: Quem instalar no Ubuntu Server, ou outra distro no modo servidor, deverá utilizar outro equipamento (ou máquina virtual) para fazer acesso a interface Web.**

* [Tutorial em Vídeo sobre a Instalação do OpenLDAP](https://www.youtube.com/watch?v=JaZuLHDQkSU) - **Excelente sugestão do colega Pablo Lopes**

#### Opção de Interface para Gerência Web do OpenLDAP
* [LDAP Account Manager](https://computingforgeeks.com/install-and-configure-ldap-account-manager-on-ubuntu/)


## Outras Informações Referentes ao Projeto Integrador (Não Serão Cobradas nas Entregas)

#### Servidor de Teste: (aguardar definição)
* URL: http://9.9.9.9/phpldapadmin/
* Username: cn=admin,dc=projeto,dc=integrador,dc=br
* Password: **enviada por email**

#### Instalando o OpenLDAP - Cliente
* [Configure Linux Clients To Authenticate Using OpenLDAP](https://www.unixmen.com/configure-linux-clients-to-authenticate-using-openldap/)

#### Utilizando Equipamentos em Nuvem
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
   
 * https://comunidade.gerenciandoweb.com.br/t/comando-para-gerenciar-uma-instancia-para-sempre-gratis-na-oracle-cloud/1622   
   * sudo apt-get update
   * sudo apt install firewalld
   * sudo firewall-cmd --zone=public --permanent --add-port=PORTA/tcp
   * sudo firewall-cmd --reload
   * sudo firewall-cmd --zone=public --list-ports
 
#### Provedores de IAAS em Cloud
* https://www.cloudatcost.com/
* https://www.oracle.com/
 
#### LDAP em Nuvem
* [jumpcloud](https://jumpcloud.com/)

 #### Introdução ao LDAP por Bolsista do G3PD
 * [Material Organizado por Ronaldo Cunha - Bolsisa G3PD](http://olaria.ucpel.edu.br/rcunha/)
