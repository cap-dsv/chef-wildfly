# Wildfly Cookbook
Cookbook para deploy de App Java no Wildfly

# Requirementos
Chef Client 11+

Java Opscode Community Cookbook

# Plataforma
- CentOS, Red Hat, Fedora
- EC2 Amazon Linux AMI
- Debian

Tested on:
- Ubuntu (local)
- CentOS 6.5 (AWS)

# Usando
Você pode adicionar usuarios em `attributes\users.rb`

Você pode customizar a versão do Java, e o Connector/J.

# Atributos - Attributes
* `node['wildfly']['base']` - Base directory to run Wildfly from

* `node['wildfly']['version']` - Specify the version of Wildfly
* `node['wildfly']['url']` - URL to Wildfly tarball
* `node['wildfly']['checksum']` - SHA256 hash of said tarball

* `node['wildfly']['user']` - User to run Wildfly as.
* `node['wildfly']['group']` - Group which owns Wildfly directories
* `node['wildfly']['server']` - Name of service and init.d script for daemonizing

* `node['wildfly']['mysql']['enabled']` - Boolean indicating Connector/J support

* `node['wildfly']['int'][*]` - Various hashes for setting interface & port bindings

* `node['wildfly']['smtp']['host']` - SMTP Destination host
* `node['wildfly']['smtp']['port']` - SMTP Destination port


# Receitas - Recipes
* `::default` - Instala Java & Wildfly.  Also installs Connector/J if you've got it enabled.
* `::install` - Instala Wildfly.
* `::mysql_connector` - Instala Connector/J no diretorio do Wildfly.

#Fork para
Equipe de Desenvolvimento do CAP.

# Autor Original:
Author:: Brian Dwyer - Intelligent Digital Services
