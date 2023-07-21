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

## Data Binding

### Interpolação

 Tem a saída de uma variável, pode também realizar expressões dentro da interpolação e colocar expressões lógicas também

{{ 1 + 1 + getValor() }}

{{ valor }}

### Property Binding

O foco é maior na propriedade, exemplo de uso

[propriedade] = “valor”

```jsx
<img [src] = "urlImagem">
```

(evento)=”handler”

[(ngModel)] = “propriedade” → Útil para formulários

### Class e Style Binding

<aside>
💡  Trabalhando com comboBox utilizando property binding e class binding

</aside>

```jsx
<h3>Class e Style Binding</h3>
    <div>
      Selecione uma classe:
      <select #classe (change)="0">
        <option value="alert-success">Sucesso</option>
        <option value="alert-info">Info</option>
        <option value="alert-warning">Alerta</option>
        <option value="alert-danger">Erro</option>
      </select>
      <br><br>

      <div class="alert {{ classe.value }}" role="alert">
        Texto colorido conforme valor do combobox.
      </div>

      <div class="alert" role="alert"
        [class.alert-success]="classe.value == 'alert-success'">
        Sucesso
      </div>

      <div class="alert" role="alert"
      [class.alert-info]="classe.value == 'alert-info'">
        Info
      </div>

      <div class="alert" role="alert"
      [class.alert-warning]="classe.value == 'alert-warning'">
        Alerta
      </div>

      <div class="alert" role="alert"
      [class.alert-danger]="classe.value == 'alert-danger'"
      >
        Erro
      </div>

      <div class="alert alert-danger" role="alert"
        [style.display]="classe.value == 'alert-danger' ? 'block' : 'none'">
        Esse texto somente aparece em caso de erro.
      </div>

    </div>
  </article>

</section>
```

Para criar uma variavel local é só colocar o “#” antes do nome da variavel e o evento logo em seguida
