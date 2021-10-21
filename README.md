# kabug-rb
Reposotorio do projeto kabug com Cucumber, capybara e ruby

## Como Executar o projeto

* Importante ter o ruby instalado(versao 2.5 ou superior)

### Instalar o Bundler
`
 gem install bundler
`
 
 ### Instalar as dependencias do roby (projeto)
`
 bundler install
`
 ### Executar localmente (minha maquina)
`
 bundler exec cucumber
`
 
 ### Executar no servidor de CI (gerando reports JSON)
`
 bundler exec cucumber -p ci
`
