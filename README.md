# Projeto-Integrador-IV-B

### Introdução ao LDAP
* [Material Organizado por Ronaldo Cunha - G3PD](http://olaria.ucpel.edu.br/rcunha/)

### Instalando o OpenLDAP - Servidor
* [Tutorial em Portugues para instalar o OpenLDAP e o phpLDAPadmin](https://www.zentica-global.com/pt/zentica-blog/ver/como-instalar-openldap-e-phpldapadmin-no-ubuntu-server-20.04-60737ebe0b7a3)
* [Tutorial em Inglês para Instalação do OpenLDAP e do phpLDAPadmin](https://idroot.us/install-openldap-ubuntu-20-04/)

### Instalando o OpenLDAP - Cliente
* [Configure Linux Clients To Authenticate Using OpenLDAP](https://www.unixmen.com/configure-linux-clients-to-authenticate-using-openldap/)

### Utilizando Equipamentos em Nuvem
* [Plataforma da Oracle](https://www.oracle.com/br/index.html)
* https://www.oracle.com/br/cloud/free/?source=:ow:o:h:feb::OHPpn1030&intcmp=:ow:o:h:feb::OHPpn1030
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
 
### LDAP em Nuvem
* [jumpcloud](https://jumpcloud.com/)
