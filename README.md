# React: Testes de Integração e Mocks no Frontend
Curso Alura

## Notas: 

### BrowserRouter 

- Componente fornecido pelo React Router
- Usado para envolver os componentes da aplicação React e permitir que sejam renderizados com base nas URLs do navegador
- Para testar componentes que usam o React Router é possível usar ferramentas como 'react-router-dom' e 'react-router' para simular o roteamento e testar como os componentes são renderizados com base nas URLs. 

### MemoryRouter

- Componente fornecido pelo React Router
- Permite o roteamento de aplicativos React em memória, sem nescessidade de usar o navegador ou alterar a base de endereço
- Útil para testar componentes React que dependem do roteamento

### Testando componentes

Para testar componentes que dependem do 'location' do usuário(ou seja, da localização atual da URL)

Opções de exemplo:

1. Usando o 'react-router-dom' e 'memory-router'
2. Mocking 'UseLocation' com 'Jest.mock'

---
>Os Hooks fornecidos pelo 'react-router-dom' são uma série de funções que permitem que você acesse o estado e a funcionalidade de roteamento ro React Route dentro de um componente funcional do React
**Alguns dos principais hooks:**
- `UseParams()`
- `UseLocation()`
- `UseHistory()`
- `UseRouteMatch()`
---

Para testar componentes que dependem de hooks fornecidos pelo 'react-router-dom' é possível utilizar técnicas de mock para simular o comportamento desses hooks durante os testes. 

### Teste de integração entre páginas

Para testar a integração entre páginas é possível no teste buscarpor um elemento que existe apenas na página que irá direcionar mediante a uma ação. 

Ex: Clique em um botão

Ao procurar pelo elemento usar o find, não esquecendo de adicionar o await antes do mesmo e de tornar o teste assíncrono com o async.

### Hooks do Jest

Esses hooks ou ganchos são funções qie executam um trecho de qualquer codigo em certa etapa do "ciclo de vida" dos testes. 

Não podem ser chamados dentro de um test!

Alguns deles: 

- beforeAll : Serve para executar algo antes da execução de todos os testes;
- beforeEach: Serve para executar algo antes da execução de cada um dos testes iniciar;
- afterAll: Serve para executar algo após a finalização de todos os testes;
- afterEach: Serve para executar algo após a finalização de cada um dos testes.

**Exemplo de uso:**

- beforeEach: limpar o mock de chamada a api antes de cada teste

---

#### *A dificuldade de testar Hooks é que eles não podem ser chamados fora de componentes React.*

---

- Utilizando renderHook é possível testar um hook fora de um componente React

### Utilizando o act para lidar com alterações de estados nos testes.

O act é usado principalmente para lidar com alterações de estado assíncronas ou efeitos colaterais durante os testes, garantindo que o componente seja atualizado de forma síncrona antes de fazer as asserções. Isso ajuda a evitar erros comuns relacionados ao timing de atualizações de estado em testes de componentes React.

### Medindo Qual a Porcentagem da Aplicação Foi Testada

No terminal escrever o comando: 

`npm run test:coverage`

Entendendo a tabela(explicação detalhada): 

- File: na primeira coluna, temos os arquivos que estão sendo testados. Todos os arquivos que terminam com .jsx ou .js. Teremos os componentes, as páginas, os hooks, a parte da API.

- %Stmts: na segunda coluna, temos os statements, que são as declarações de variáveis e outras coisas que estão sendo testadas durante a execução dos testes.

- %Branch: na terceira coluna, estão as branches, que são, basicamente, as declarações, os blocos de código if e else.

- %Funcs: na quarta coluna, temos as funções que estão sendo executadas durante os testes.

- % Lines: na quinta linha, temos a quantidade de linhas que estão sendo testadas na execução do teste.

- Uncovered Line #s: na última coluna, estão as linhas não cobertas, as linhas que não testamos, elas estão associadas aos componentes que não foram testados.

Escrever testes unitários e de integração no Front-End: <a href="https://www.alura.com.br/artigos/dicas-desenvolver-testes-unitarios-integracao-front-end?utm_source=gnarus&utm_medium=timeline">Dicas</a>