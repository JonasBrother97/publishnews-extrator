# PublishNews-Extrator

Nosso projeto consiste em facilitar o acesso aos dados do site [PublishNews](https://www.publishnews.com.br/ranking).
O site PublishNews apresenta relatórios semanais, mensais e anuais sobre os livros mais vendidos através de uma amostra enviada por diversos lojistas/livrarias. 

## Requirements

* selenium
'''
pip install selenium
'''
* webdriver_manager
'''
pip install webdriver_manager
'''
### Optional (for better visualization)

* pandas
'''
pip install pandas
'''

## Installation

* Clone the repository
'''
git clone git@github.com:JonasBrother97/publishnews-extrator.git
'''

* Pip
'''
pip install publishnewsextratorp
'''

## Usage

* Chamando as classes da biblioteca publishnewsextratorp
'''
from publishnewsextratorp.file1 import IniciarDriver, ExcecaoAnoInvalido, ExtracaoPublishNews
'''

* Instancia a classe para abrir o driver, exibe a mensagem caso o driver esteja atualizado ou baixa automaticamente caso não esteja.
'''
exemplo = ExtracaoPublishNews()
'''

* Método para selecionar o ano, não é necessário passar argumento
'''
exemplo.seleciona_anual()
'''

* Ou método para escolher o ano, necessário passar como argumento o ano escolhido, entre 2010 e 2021 (são os anos dispoíveis no site)
'''
exemplo.seleciona_ano(2019)
'''

* Coleta os dados e guarda no dataFrame, necessário guardar o dataframe que retorna da classe dentro de uma variavel
'''
dataFrame_exemplo = exemplo.coleta_dados()
'''

* Exibindo o dataframe
'''
dataFrame_exemplo
'''

* Salvar o arquivo em excel
'''
exemplo.salvar_dataframe(dataFrame_exemplo, 'df_exemplo')
'''

* Fechar aba do chrome
'''
exemplo.fecha_browser()
'''