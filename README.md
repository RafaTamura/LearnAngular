# Angular
Confira a documentação aqui
https://angular.io

Parceria entre Google e Microsoft 

Foi criado para ser escrito em typescript

## Component

O angular é orientado a componentes, ele possui um componente raiz que pode possuir outros componentes, quebra a aplicação em pequenas partes

Encapsula

- Template
- Metadata: processamento das classes
- Dado a ser mostrado na tela
- Comportamento da View

## Router

Responsável pela navegação, realiza o roteamento das páginas

## Diretivas

Responsável por modificar elementos DOM da página

# Ambiente de Desenvolvimento

1 - Instalar o Node.js no próprio site do [nodejs.org](http://nodejs.org) 

2 - Instalar o Angular pelo terminal 

- npm install -g @angular/cli

3 - Para testar se o angular está instalado é só conferir a versão com 

- ng version

4 - Criar um projeto 

- ng new

5 - Abrir o localhost

- ng serve

### 

Toda vez que um módulo é criado é necessário declará-lo no app.module.ts

além de exportar ele na própria classe

### Criar um Componente

O componente é onde fica a lógica do projeto

- ng g c

## Módulos

Existe o módulo raiz do projeto, e os criados que são para criar as funcionalidades.

Nele só importa o CommonModule e para exportar utiliza o: 

```jsx
exports:[
componente a ser exportado
]
```

Criar um módulo

- ng g m

Para adicionar os módulos e componentes criados no app component é necessário add o seletor no app component (tag html)

## Services

O serviço é responsável por fazer a conexão com o back-end.

O HttpModule realiza a busca de dados de uma fonte externa

Criar um serviço

- ng g s

O decorator injectable indica que essa classe pode ser injetada em outra classe

providers são os serviços fornecedores
