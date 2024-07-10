# Perguntas e Respostas de Entrevistas de Emprego

## React 17 ou Superior

**Pergunta:** O que são hooks no React e como eles diferem dos componentes de classe?

**Resposta:** Hooks são funções que permitem que você use o estado e outros recursos do React sem escrever uma classe. Eles foram introduzidos no React 16.8. Hooks como `useState` e `useEffect` são comumente usados para gerenciar estado e efeitos colaterais em componentes funcionais, tornando o código mais simples e fácil de entender em comparação com componentes de classe.


**Pergunta:** Explique o conceito de Virtual DOM no React.

**Resposta:** O Virtual DOM é uma representação leve do DOM real. Quando o estado de um componente muda, o React cria um novo Virtual DOM e o compara com o anterior. Apenas as diferenças são atualizadas no DOM real, o que torna a atualização da interface do usuário mais eficiente.

## .NET Core - C#

**Pergunta:** O que é o .NET Core e quais são suas vantagens em relação ao .NET Framework?

**Resposta:** O .NET Core é uma plataforma de desenvolvimento de código aberto e multiplataforma para a construção de aplicativos modernos, baseados na nuvem e IoT. Suas vantagens incluem ser multiplataforma (funciona no Windows, macOS e Linux), ter melhor desempenho e ser modular, permitindo que os desenvolvedores escolham apenas os pacotes necessários.


**Pergunta:** Explique o conceito de async/await no C#.

**Resposta:** `async` e `await` são palavras-chave no C# que permitem escrever código assíncrono de maneira mais simples e legível. `async` é usado para marcar um método como assíncrono, enquanto `await` é usado para esperar a conclusão de uma tarefa assíncrona, sem bloquear o thread principal.

## SQL Server T-SQL

**Pergunta:** O que é uma procedure no SQL Server e qual é sua utilidade?

**Resposta:** Uma procedure (procedimento armazenado) é um conjunto de instruções SQL pré-compiladas armazenadas no banco de dados. Elas são usadas para executar tarefas repetitivas e complexas de forma eficiente, melhorar a segurança e permitir a reutilização de código.


**Pergunta:** Como você pode otimizar consultas T-SQL para melhorar o desempenho?

**Resposta:** Para otimizar consultas T-SQL, você pode criar índices apropriados, evitar o uso de `SELECT *`, usar joins corretamente, particionar tabelas grandes, analisar e otimizar planos de execução e evitar operações de loop aninhadas.

## RabbitMQ

**Pergunta:** O que é RabbitMQ e para que ele é usado?

**Resposta:** RabbitMQ é um broker de mensagens que facilita a comunicação entre diferentes sistemas e aplicativos por meio de filas de mensagens. Ele é comumente usado em arquiteturas de microserviços para garantir a entrega de mensagens de maneira confiável e eficiente.


**Pergunta:** Qual a diferença entre um Exchange e uma Queue no RabbitMQ?

**Resposta:** Um Exchange é responsável por receber mensagens de produtores e roteá-las para as filas (Queues) de acordo com regras específicas (bindings). As Queues armazenam e gerenciam as mensagens até que sejam consumidas pelos consumidores.

## Git

**Pergunta:** O que é Git e por que ele é usado no desenvolvimento de software?

**Resposta:** Git é um sistema de controle de versão distribuído que permite aos desenvolvedores rastrear mudanças no código, colaborar com outros e gerenciar diferentes versões de um projeto. Ele é usado para facilitar o desenvolvimento colaborativo e manter um histórico detalhado de todas as alterações no código.


**Pergunta:** Explique a diferença entre `git merge` e `git rebase`.

**Resposta:** `git merge` combina duas ramificações (branches) diferentes, criando um novo commit de merge. `git rebase` move ou combina uma sequência de commits para uma nova base, criando um histórico linear. `rebase` é útil para manter um histórico de commits mais limpo, enquanto `merge` preserva o histórico original.

## Dapper

**Pergunta:** O que é Dapper e quais são suas vantagens em relação ao Entity Framework?

**Resposta:** Dapper é um micro ORM (Object-Relational Mapper) para .NET que facilita a execução de consultas SQL diretamente e mapeia os resultados para objetos C#. Suas vantagens incluem melhor desempenho e menor sobrecarga em comparação com o Entity Framework, tornando-o ideal para cenários onde o desempenho é crítico.


**Pergunta:** Como você executa uma consulta SQL com parâmetros usando Dapper?

**Resposta:** Para executar uma consulta com parâmetros usando Dapper, você pode usar o método `Query` ou `Execute` fornecendo a consulta SQL e um objeto anônimo com os parâmetros:
```csharp
using (var connection = new SqlConnection(connectionString))
{
    var result = connection.Query<YourEntity>("SELECT * FROM YourTable WHERE Id = @Id", new { Id = id });
}
```

## Entity Framework

**Pergunta:** O que é Entity Framework e qual é sua principal funcionalidade?

**Resposta:** Entity Framework (EF) é um ORM para .NET que permite aos desenvolvedores trabalhar com um banco de dados usando objetos .NET. Sua principal funcionalidade é mapear entidades de banco de dados para objetos C#, facilitando o desenvolvimento de aplicativos baseados em dados sem escrever consultas SQL complexas.


**Pergunta:** Explique a diferença entre abordagem Code-First e Database-First no Entity Framework.

**Resposta:** Na abordagem Code-First, você define suas classes de modelo em código e o Entity Framework gera o banco de dados com base nesses modelos. Na abordagem Database-First, você cria o banco de dados primeiro e o Entity Framework gera as classes de modelo a partir das tabelas e colunas existentes.

## Next.js

**Pergunta:** O que é Next.js e quais são suas principais características?

**Resposta:** Next.js é um framework React para construção de aplicações web com renderização do lado do servidor (SSR) e geração de sites estáticos. Suas principais características incluem roteamento baseado em páginas, suporte a CSS e Sass, otimização automática de imagens e integração com API Routes para criar endpoints backend.


**Pergunta:** Como você cria uma página estática em Next.js?

**Resposta:** Para criar uma página estática em Next.js, você pode usar a função `getStaticProps` para gerar conteúdo estático durante a build:
```javascript
export async function getStaticProps() {
  // Fetch data from an API or database
  const data = await fetchData();
  return {
    props: { data },
  };
}

export default function Page({ data }) {
  // Render the page with the fetched data
  return <div>{data.content}</div>;
}
```

## Microservices

**Pergunta:** O que é uma arquitetura baseada em microserviços e quais são suas vantagens?

**Resposta:** Uma arquitetura baseada em microserviços divide um aplicativo em pequenos serviços independentes que se comunicam entre si por meio de APIs. Suas vantagens incluem escalabilidade, facilidade de manutenção, implantação independente e maior resistência a falhas.


**Pergunta:** Quais são os desafios comuns ao trabalhar com microserviços?

**Resposta:** Os desafios comuns incluem a complexidade de gerenciamento de múltiplos serviços, latência de comunicação entre serviços, consistência de dados, monitoramento e logging distribuído e implementação de segurança.

## Azure DevOps

**Pergunta:** O que é Azure DevOps e quais são seus principais componentes?

**Resposta:** Azure DevOps é um conjunto de ferramentas de desenvolvimento que suporta todo o ciclo de vida do desenvolvimento de software. Seus principais componentes incluem Azure Boards (gerenciamento de projetos), Azure Repos (controle de versão), Azure Pipelines (CI/CD), Azure Test Plans (testes) e Azure Artifacts (gerenciamento de pacotes).


**Pergunta:** Como você configura uma pipeline de CI/CD no Azure DevOps?

**Resposta:** Para configurar uma pipeline de CI/CD, você precisa definir um arquivo YAML que descreve as etapas de build e deploy, e configurar os gatilhos para iniciar a pipeline:
```yaml
trigger:
- main

pool:
  vmImage: 'ubuntu-latest'

steps:
- task: UseDotNet@2
  inputs:
    packageType: 'sdk'
    version: '5.x'
    installationPath: $(Agent.ToolsDirectory)/dotnet

- script: dotnet build --configuration Release
  displayName: 'Build project'

- script: dotnet publish --configuration Release --output $(Build.ArtifactStagingDirectory)
  displayName: 'Publish project'

- task: PublishBuildArtifacts@1
  inputs:
    PathtoPublish: '$(Build.ArtifactStagingDirectory)'
    ArtifactName: 'drop'
    publishLocation: 'Container'
```

## Docker

**Pergunta:** O que é Docker e quais são seus benefícios?

**Resposta:** Docker é uma plataforma que permite criar, implantar e executar aplicativos em contêineres. Os benefícios incluem portabilidade (executar aplicativos em qualquer ambiente que suporte Docker), isolamento (contêineres são independentes uns dos outros), escalabilidade (facilmente criar múltiplas instâncias de contêineres) e eficiência (contêineres compartilham o mesmo sistema operacional).


**Pergunta:** Como você cria um Dockerfile básico para um aplicativo .NET Core?

**Resposta:** Um Dockerfile básico para um aplicativo .NET Core pode ser assim:
```dockerfile
# Use a imagem base do .NET Core SDK
FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build
WORKDIR /app

# Copie e restaure os pacotes NuGet
COPY *.
```

## Java

**Pergunta:** O que é a JVM e qual é a sua função?

**Resposta:** A JVM (Java Virtual Machine) é uma máquina virtual que permite a execução de programas Java. Sua função principal é converter bytecode Java em código de máquina que pode ser executado pelo sistema operacional, garantindo a portabilidade do código Java entre diferentes plataformas.


**Pergunta:** O que é o Garbage Collection no Java?

**Resposta:** Garbage Collection é um processo automático de gerenciamento de memória que remove objetos que não são mais referenciados pelo programa, liberando espaço na memória heap e prevenindo vazamentos de memória.

## Python

**Pergunta:** Qual a diferença entre listas e tuplas em Python?

**Resposta:** A principal diferença é que listas são mutáveis, o que significa que seus elementos podem ser alterados, adicionados ou removidos. Já as tuplas são imutáveis, ou seja, uma vez criadas, seus elementos não podem ser modificados.


**Pergunta:** O que são list comprehensions em Python?

**Resposta:** List comprehensions são uma forma concisa de criar listas. Elas permitem construir listas de forma compacta e legível, utilizando uma expressão seguida por um loop for.

**Exemplo:**
```python
squares = [x**2 for x in range(10)]
```

## PHP

**Pergunta:** O que é PHP e para que ele é usado?
**Resposta:** PHP (Hypertext Preprocessor) é uma linguagem de script de código aberto amplamente usada para desenvolvimento web. Ele é executado no servidor e é capaz de gerar conteúdo dinâmico para páginas web.

**Pergunta:** Como você conecta ao banco de dados MySQL usando PHP?
**Resposta:** Você pode usar a extensão mysqli ou PDO para conectar ao MySQL. Aqui está um exemplo usando mysqli:
```php
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "database";

$conn = new mysqli($servername, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
echo "Connected successfully";
```

## Spring Boot (Java)

**Pergunta:** O que é Spring Boot e quais são suas vantagens?
**Resposta:** Spring Boot é um framework baseado em Java que simplifica o processo de configuração e implementação de aplicativos Spring. Suas vantagens incluem configuração automática, um servidor embutido para testes e produção, e a capacidade de criar aplicativos stand-alone.

**Pergunta:** Como você define um controlador REST no Spring Boot?
**Resposta:** Você define um controlador REST usando a anotação `@RestController` e mapeia as rotas com `@RequestMapping` ou `@GetMapping`, `@PostMapping`, etc.
```java
@RestController
@RequestMapping("/api")
public class MyController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, World!";
    }
}
```

## Python Pandas

**Pergunta:** O que é o Pandas e para que ele é usado?
**Resposta:** Pandas é uma biblioteca de código aberto para a linguagem Python, amplamente utilizada para análise de dados e manipulação de dados. Ele fornece estruturas de dados e funções que facilitam a limpeza, transformação, agregação e visualização de dados.

**Pergunta:** Como você lê um arquivo CSV usando Pandas?
**Resposta:** Você pode usar a função `read_csv` para ler um arquivo CSV:
```python
import pandas as pd

df = pd.read_csv('file.csv')
print(df.head())
```

## Flask (Python)

**Pergunta:** O que é Flask e para que ele é usado?
**Resposta:** Flask é um microframework web escrito em Python. Ele é usado para desenvolver aplicações web leves e rápidas, oferecendo as ferramentas necessárias para construir um servidor web sem impor muitas restrições ou dependências.

**Pergunta:** Como você cria uma rota simples em Flask?
**Resposta:** Você cria uma rota simples usando a anotação `@app.route` e definindo uma função para lidar com as solicitações.
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(debug=True)
```

## Django (Python)

**Pergunta:** O que é Django e quais são suas principais características?
**Resposta:** Django é um framework web de alto nível para Python que promove o desenvolvimento rápido e um design limpo e pragmático. Suas principais características incluem um ORM poderoso, administração automática, autenticação de usuários, e suporte a templates.

**Pergunta:** Como você cria um modelo (model) em Django?
**Resposta:** Você cria um modelo definindo uma classe que herda de `models.Model` e define atributos que correspondem a campos do banco de dados.
```python
from django.db import models

class MyModel(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()

    def __str__(self):
        return self.name
```
