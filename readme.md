## Primero passo
* criar pastas com o comando mkdir
* Explicação do comando: mk = make dir = pasta => criar nova pasta

## Segundo Passo
* o comando cd projetoBackend  = acesssa a pasta que foi criada, trocando o nome da pasta original "novoaula" por "projetoBackend"

## Terceiro passo
* touch readme.md = usado para criar um novo arquivo vazio com o nome especificado, no caso "readme.md" 
* touch": ele é usado para criar arquivos vazios ou atualizar os timestamps (carimbos de data e hora) de arquivos existentes. 
* "readme.md": Este é o argumento que segue o comando "touch". É o nome do arquivo que você deseja criar. 
* O ".md" na extensão do arquivo indica que este é um arquivo Markdown, frequentemente usado para documentação em formato de texto simples com formatação.

## Quarto passo
### npm init -y =
* "npm": Este é o comando principal da ferramenta Node Package Manager (npm), que é amplamente utilizado para gerenciar pacotes e dependências em projetos Node.js.
* "init": Este é um subcomando do npm que é usado para iniciar a criação de um novo projeto Node.js. Ele faz uma série de perguntas interativas para coletar informações, como o nome, a versão, a descrição, o ponto de entrada, as dependências, e etc.
* "-y": O argumento "-y" é uma opção que você pode fornecer ao subcomando "init". Essa opção indica ao npm para aceitar automaticamente todas as opções padrão ao criar o arquivo "package.json" e não pedir que você forneça respostas interativas para cada pergunta. 

## Quinto passo
* "npm": Este é o comando principal da ferramenta Node Package Manager (npm), que é usada para gerenciar pacotes e dependências em projetos Node.js.
* "i" (ou "install"): A opção "i" = abreviação de "install". Ela indica ao npm que você deseja instalar pacotes no projeto.
* "express": O Express.js é um popular framework de aplicativo web para Node.js que facilita a criação de aplicativos web robustos e eficientes. 
* "nodemon": O nodemon é uma ferramenta de desenvolvimento que monitora as alterações nos arquivos do seu projeto Node.js e reinicia automaticamente o servidor sempre que você faz uma alteração no código.
* "dotenv": O dotenv é um pacote que permite carregar variáveis de ambiente a partir de um arquivo chamado ".env" no seu projeto.

## Sexto passo
* comando "code ." abre o vscode com as abas "package-lock.json" e "package.json" abertas.

## Sétimo passo 
* nano .gitignore = abre o editor de texto "nano" com o arquivo chamado ".gitignore". Esse arquivo é usado em projetos Git para listar os arquivos e diretórios que você deseja que o Git ignore.
* pode adicionar nomes de arquivos, padrões ou diretórios inteiros ao ".gitignore" para evitar que eles sejam incluídos no controle de versão do Git. Essa é uma prática comum para evitar que arquivos temporários, arquivos de compilação

## Oitavo passo
* node_modules = um diretório que é comumente encontrado em projetos Node.js. Ele é usado para armazenar as dependências (ou pacotes) que um projeto Node.js utiliza. 
* O diretório "node_modules" contém os arquivos de código fonte dos pacotes instalados e suas dependências, permitindo que o projeto acesse essas bibliotecas.

## Nono passo 
* O comando "mkdir src" é usado para criar um novo diretório chamado "src" no sistema de arquivos. Esse diretório "src" geralmente é usado em projetos de software para armazenar arquivos de código-fonte (source code), como scripts, classes, módulos ou outros componentes do programa. 
* É uma prática comum organizar o código-fonte em um diretório "src" para manter os arquivos relacionados ao código central do projeto separados de outros recursos ou arquivos de configuração.

## 11º passo
* O comando "touch src/app.js" cria um novo arquivo vazio chamado "app.js" no diretório "src" dentro do sistema de arquivos. 
* Esse comando é frequentemente usado para criar rapidamente um arquivo de código-fonte ou um ponto de entrada para um aplicativo em desenvolvimento.

## 12º passo
* cria um novo arquivo vazio chamado "server.js" no diretório "src" dentro do sistema de arquivos.
* Esse comando é frequentemente usado para criar rapidamente um arquivo que pode servir como ponto de entrada para um servidor ou aplicativo em desenvolvimento.

# Passo 2 - 02/10

* Copiar a url do projeto
Acessar repositório do projeto no gitHub
Clicar no botão verde '<> Code'
Clicar no ícone para copiar a URL, conforme a imagem

* Clonar o repositório na sua máquina
Abrir o gitBash em um local do computador
Digitar o comando 'git clone' junto com a URL do seu repositório = git clone URL_REPOSITORIO

* Acessar pasta
Digitar o comando 'cd' e o nome do seu repositório
cd (change directory): acessar outra pasta = cd NOME_REPOSITORIO

* Reinstalar os pacotes da aplicação = npm i

* Criar arquivo .env na raiz do projeto
Este arquivo é utilizada para armazenar as variáveis que serão reutilizadas na aplicação
Com o comando nano, podemos criar e editar um arquivo pelo terminal
Ctrl + o: Salvar o arquivo
Enter: Confirmar
Ctrl + x: Fechar o arquivo = * nano .env

* Digitar no arquivo .env = PORT = 3008
* ma
* Adicionar arquivo .env no .gitignore = nano .gitignore, = .env
* Abrir o VSCode = code .

* Criar arquivo de exemplo para para as variáveis necessárias da aplicação
Como não enviamos o arquivo .env para o gitHub, precisamos criar o exemplo das variáveis necessárias da aplicação
Este arquivo conterá apenas as variáveis, sem os valores correspondentes = nano .env.example

* Adicionar no arquivo .env.example = PORT = 
* Abrir o arquivo app.js e digitar o código 

* Importar o pacote express (servidor) = const express 

* Importar o pacote dotenv, gerenciador de variáveis de ambiente = const dotenv = require('dotenv').config();

* Instanciar o express na variável app = const app = express();

* Setar a porta do servidor a partir do arquivo .env
O operador condicional '||' significa 'OU', caso não tenha a variável PORT, será utilizado o valor '3333' = app.set('port', process.env.PORT || 3333); 
* Exportar as configurações na variável app = module.exports = app;
* Abrir o arquivo server.js e digitar os códigos
Importar o arquivo app = const app = require('./app');
* Importar a porta do servidor = const port = app.get('port');

* Testar API com a função listen
1º parâmetro: passamos a porta do servidor
2º parâmetro: arrow function para retornar um console informando a porta que está rodando o servido = app.listen(port, () => {
    console.log(`Running on port ${ port }!`);
});
* Depois de configurar os pacotes e o teste do servidor, vamos criar o comando para executar
Abrir o arquivo package.json e alterar a chave 'scripts'
Substituir o comando 'test' pelo comando 'start' na linha = "start":"nodemon src/server.js"
* Rodar o comando no termial com gitBash = npm run start
* Atualizar projeto no gitHub
* Adicionar todos arquivos ao versionamento = git add .
* Salvar projeto e escrever comentário sobre o processo realizado = git commit -m 'configuração do projeto'
* Enviar os arquivos atualizados para o gitHub = git push
* Atualize a página no gitHub e verifique se os arquivos foram atualizados
Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina = cd ..
* Comando para acessar uma pasta anterior
Fechar o VSCode com o projeto aberto
* rm -rf projetoBackend
* rm (remove): comando utilizado para apagar arquivo
* -r (recursive): apaga pastas e subpastas de forma recursiva
* -f (force): não pergunta confirmações
* projetoBackend: nome da pasta que contem os arquivos da aplicação

* Conclusão do Passo 2
URL do repositório com:
Estrutura do projeto
Arquivo readme de documentação dos passos realizados
Configuração
Retorno de teste da API
Enviar a URL na tarefa do teams
Tarefa 2 - Configuração inicial

* passo 3 09/10
* Clonar o projeto do gitHub, criar a configuração do arquivo de rotas
Comando clone do git
Configurar arquivo routes
Copiar a url do projeto
Acessar repositório do projeto no gitHub
Clicar no botão verde '<> Code'
Clicar no ícone para copiar a URL, conforme a imagem

* Clonar o repositório na sua máquina
Abrir o gitBash em um local do computador
Digitar o comando 'git clone' junto com a URL do seu repositório

* Acessar pasta
Digitar o comando 'cd' e o nome do seu repositório
cd (change directory): acessar outra pasta

* Reinstalar os pacotes da aplicação
npm i
Este comando irá recriar a pasta node_modules no projeto

* Criar pastas dentro da pasta src
mkdir src/routes

* Criar arquivo dentro da pasta routes
touch src/routes/rotas.js
Responsável pelas rotas que serão acessadas na API

* Abrir o VSCode
code .
* Abrir o arquivo rotas.js e digitar os códigos
// Importar o modulo de Router do express
const { Router } = require('express');

// Instanciar o Router na variável router
const router = Router();

router.get('/listar', (request, response) => {
    response.send('Método GET: listar informações');
});
router.post('/cadastrar', (request, response) => {
    response.send('Método POST: salvar informações');
});
router.put('/user/:id', (request, response) => {
    response.send('Método PUT: atualizar informações');
});
router.delete('/user/:id', (request, response) => {
    response.send('Método DELETE: remover informações');
});

module.exports = router;
* Abrir o arquivo app.js e adicionar o código
Precisamos importar o arquivo de rotas nas configurações da API
const router = require('./routes/rotas');
Habilitar as rotas na aplicação
Esta linha deve inserida depois da criação da variável app
app.use('/api', router);
* Atualizar projeto no gitHub
Adicionar todos arquivos ao versionamento
git add .
* Salvar projeto e escrever comentário sobre o processo realizado
git commit -m 'rotas do projeto'
* Enviar os arquivos atualizados para o gitHub
git push
* Atualize a página no gitHub e verifique se os arquivos foram atualizados
Com o projeto no servidor remoto podemos remover os arquivos na nossa máquina
cd ..
* Comando para acessar uma pasta anterior
Fechar o VSCode com o projeto aberto
rm -rf projetoBackend
* rm (remove): comando utilizado para apagar arquivo
-r (recursive): apaga pastas e subpastas de forma recursiva
-f (force): não pergunta confirmações
projetoBackend: nome da pasta que contem os arquivos da aplicação
* Conclusão do Passo 3
URL do repositório com:
Estrutura do projeto

* Arquivo readme de documentação dos passos realizados
Configuração
Retorno de teste da API
Arquivo de rotas com os métodos [GET, POST, PUT, DELETE]
Enviar a URL na tarefa do teams