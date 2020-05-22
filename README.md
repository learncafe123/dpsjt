# DPSJT (Depósito de Materiais de Construção São Judas Tadeu)
Website desenvolvido utilizando Python e Flask. Planejado para a exibição de informações da empresa de interesse de clientes e fornecedores, além de possuir um sistema de acesso aos produtos do depósito, com a possibilidade de leitura, inserção e alteração de produtos.

### Diretório
No download, você encontrará os seguintes diretórios e arquivos:
```
dpsjt/
│── db/
│   │── data.sql
│   └── product.sql
│── static/
│   │── bootstrap.min.css
│   │── bootstrap.min.js
│   │── dpsjt.png
│   │── jquery.min.js
│   │── jquery.tablesorter.min.js
│   │── logo.png
│   │── logo.psd
│   │── logo.svg
│   │── luiz_amichi.svg
│   │── padlock.svg
│   └── trowel.svg
│── templates/
│   │── error.html
│   │── index.html
│   │── login.html
│   └── system.html
│── dpsjt.py
│── product.py
└── README.md
```

### Dependências
Para o funcionamento do software, é necessário possuir o [Python 3](https://www.python.org/) e o [SQLite](https://www.sqlite.org/) instalado na máquina. Além do interpretador e da biblioteca, são necessários alguns pacotes ([Flask](https://flask.palletsprojects.com/en/1.1.x/) e [Jinja](https://jinja.palletsprojects.com/en/2.11.x/)) que podem ser instalados através do [PIP](https://pypi.org/project/pip/).
Instale as dependências para iniciar o servidor, abaixo é informado o passo a passo para a preparação do ambiente em Linux.
```sh
$ sudo apt update
$ sudo apt install python3 sqlite3
$ sudo apt -y install python3-pip
$ pip install -U Flask Jinja2
```


### Instalação
Após ter todas as dependências instaladas, basta clonar o repositório e inicar o software. Lembrando que a primeira execução do software utiliza um comando diferente, informando o argumento (*initdb*).
```sh
$ git clone https://github.com/luizamichi/dpsjt
$ cd dpsjt
```

Primeira inicialização do software com a base de dados vazia:
```sh
$ python3 dpsjt.py initdb
```

Primeira inicialização do software com a base de dados populada com alguns produtos para fins de teste:
```sh
$ python3 dpsjt.py initdb populate
```

Modo *debug*:
```sh
$ python3 dpsjt.py debug
```

Modo *release*:
```sh
$ python3 dpsjt.py
```

Caso aconteça algum problema, crie uma ambiente virtual isolado com o VENV e instale as dependências e o software nela.

O processo estará executando na porta 5000 e pode ser acessado utilizando qualquer navegador de internet.

### Caminhos
A tabela informa os endereços acessíveis:

| Rota | Descrição |
| ---- | --------- |
| / | Página inicial (Website) |
| /login | Página de autenticação |
| /system | Página de gerenciamento de produtos |