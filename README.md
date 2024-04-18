# React: Testes de Integração e Mocks no Frontend
Curso Alura - Em andamento

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

<div style="background:pink; padding:5px; color:black; margin:10px">
<p>Os Hooks fornecidos pelo 'react-router-dom' são uma série de funções que permitem que você acesse o estado e a funcionalidade de roteamento ro React Route dentro de um componente funcional do React</p>
<p>Alguns dos principais hooks:</p>
<li>UseParams()</li>
<li>UseLocation()</li>
<li>UseHistory()</li>
<li>UseRouteMatch()</li>
</div>

Para testar componentes que dependem de hooks fornecidos pelo 'react-router-dom' é possível utilizar técnicas de mock para simular o comportamento desses hooks durante os testes. 

### Teste de integração entre páginas

Para testar a integração entre páginas é possível no teste buscarpor um elemento que existe apenas na página que irá direcionar mediante a uma ação. 

Ex: Clique em um botão

Ao procurar pelo elemento usar o find, não esquecendo de adicionar o await antes do mesmo e de tornar o teste assíncrono com o async. 