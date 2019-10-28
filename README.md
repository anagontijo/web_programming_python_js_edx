# Curso EDX: CS50's Web Programming with Python and JavaScript

## 1 - Git

### 1.1 Git Add

* Comando:
    ```console
    user@linux:~$ git add file_path
    ```

    Comando para adicionar um arquivo ao _git_, para que suas mudanças sejam registradas no _git_.

* Funcionamento:
    Quando um arquivo é adicionado ao _git_ suas mudanças passam a ser rastreadas e sempre que algo é modificado em um arquivo que está no _git_ essas mudanças vão precisar ser registradas e atualizadas no repositório remoto.

### 1.2 Git Commit

* Comando:
    ```console
    user@linux:~$ git commit -m "Comentários das Alterações"
    ```

    Comando para registrar as mudanças feitas nos arquivos do _git_.

* Funcionamento:
    Quando um _commit_ é feito no _git_ as alterações são salvas no repositório local com uma mensagem relacionada as alterações feitas.

### 1.3 Git Push

* Comando:
    ```console
    user@linux:~$ git push origin master
    ```

    Comando para enviar os _commits_ para o repositório remoto.

* Funcionamento:
    Quando um grupo de _commits_ é enviado para o repositório remoto as mudanças locais se tornam globais.

### 1.4 Git Pull

* Comando:
    ```console
    user@linux:~$ git pull
    ```

    Comando para baixar as alterações feitas no repositório remoto.

* Funcionamento:
    Quando é realizado um _pull_ as mudanças globais que foram feitas por outras pessoas com acesso ao repositório remoto são trazidas para o repositório local.

### 1.5 Git Branch

* Comando:
    ```console
    user@linux:~$ git branch feature
    ```

    Comando para criar uma _branch_ no repositório local.

* Funcionamento:


## 2 - HTML e CSS

### 2.1 - HTML

#### 2.1.1 Header

#### 2.1.2 Nav

#### 2.1.3 Section

#### 2.1.4 Footer

#### 2.1.5 Form

##### 2.1.5.1 Radio

Radio é um tipo de formulário em que se fornece opções de escolha ao invés de inserção de opção.

Um exemplo é uma escolha de de cor favorita:

```html
<body>
    <form>
        <div>
            Cor favorita?
            <input name="nome" type="radio" value="w">
            <input name="nome" type="radio" value="x">
            <input name="nome" type="radio" value="y">
            <input name="nome" type="radio" value="z">
        </div>
    </form>
</body>
```

##### 2.1.5.2 List

List é um parâmetro de input que permite que um input de texto tenha opções por padrão.

```html
<body>
    <form>
        <div>
            <input name="escolha" list="opcoes" placeholder="Escolha Padrao">
            <datalist id="opcoes">
                <option value="opcao1">
                <option value="opcao2">
                <option value="opcao3">
                </option>
            </datalist>
        </div>
    </form>
</body>
```

#### 2.1.6 Listas

Para se definir listas em _html_ é possível utilizar as opções __ul__ e __ol__. UL designa _unordered list_, ou seja, lista desordenada. Usando UL são feitos tópicos sem enumeração, como:
* Lista 1
* Lista 2
* Lista 3  
Já OL designa _ordered list_, ou seja, lista ordenada. Usando OL cada um dos tópicos será enumerado:  
1 Lista I  
2 Lista II  
3 Lista III

```HTML
<ol>
    <li>item 1</li>
    <li>item 2</li>
    <li>item 3</li>
</ol>
```

### 2.2 CSS

#### 2.2.1 CSS dentro de HTML

Dentro do html é possível definir o estilo de exibição do html usando a tag _style_ e padrões de css.

```html
<head>
    <title>Titulo</title>
    <style>
        h1, h2 {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Titulo grande</h1>
    <h2>Titulo menor</h2>
</body>
```

#### 2.2.2 Padrões CSS

O padrão principal do css é:

```css
classe1, classe2 {
    color: cor;
    text-align: alinhamento;
    font-family: verdana;
    font-size: 20px;
}
```

Isso modifica as classes 1 e 2  de acordo com as definições dadas. Classes podem ser dadas como _h1_, _h2_ caso sejam classes padrão de _html_ ou como _.minha_classe_ se for um nome de classe passado como parametro.

```css
classe subclasse {
    color: cor;
    text-align: alinhamento;
    font-family: verdana;
    font-size: 20px;
}
```  

Isso modifica todas as instâncias da subclasse associada a classe, independente do nível de dependencia da subclasse.

```css
classe > subclasse {
    color: cor;
    text-align: alinhamento;
    font-family: verdana;
    font-size: 20px;
}
```  

Isso por sua vez modifica apenas a subclasse de classe imediatamente.

```css
classe[atributo=opcao] {
    background-color: red;
}
```

Isso modifica tudo na classe especificada que seja do atributo dado (opcao).

```CSS
classe:pseudoclasse {
    background-color: green;
}
```

Isso modifica a aparência da classe quando está nessa pseudoclasse. (hover)

```css
classe::pseudoclasse {
    content: "conteudo";
    font-weight: bold;
}
```

Isso insere um conteudo no pseudoelemento relativo a cada objeto dessa classe. (before, selection, after)

```css
classe subclasse1 + subclasse2 {
    color: blue;
}
```

Por fim, isso define a aparencia de ambas as subclasses.

#### 2.2.3 Compatibilidade

É possível definir estilos diferentes de CSS para classes diferentes em medias diferentes, isso é, em telas de computador, celulares, impressões...

Por exemplo, pode ser que em medias que não impressas 2 paragrafos sejam exibidos mas quando se for imprimir apenas o paragrafo 1 deve ser exibido.

```html
<head>
    <style>
        @media print {
            .screen-only {
                display: none;
            }
        }
    </style>
</head>
<body>
    <p>Paragrafo 1</p>
    <p class="screen-only">Paragrafo 2</p>
</body>
```
Também é possível definir a aparencia de acordo com atributos da media. Por exemplo, caso para exibições de largura menor que 500 pixels eu queira que a tela tenha um fundo diferente de que para maiores ou iguais.

```html
<head>
    <style>
        @media (min-width: 500px) {
            body {
                background-color: red;
            }
        }
        @media (max-width: 499px) {
            body {
                background-color: green;
            }
        }
    </style>
</head>
<body>
    <h1>Ola</h1>
    <h2>Essa página é um teste</h2>
</body>
```

A linha para que a largura da exibição seja adaptada para a largura do device é

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
##### 2.2.3.1 Flexbox

Quando se tem diferentes larguras de tela e uma estrutura que envolve exibição de itens em largura pela tela pode ser necessário que se faça adaptações para impedir que sejam necessários scrolls desconfortáveis. Para isso se define que o display é _flex_, e outros atributos são usados para definir como o display vai se adaptar a diferentes larguras.

Um exemplo é, com uma sequencia de caixas de texto padrão pode-se querer que as caixas se encaixem de forma diferente de acordo com a largura da tela, exibindo menos caixas por linha de acordo com a disponibilidade de espaço.

```html
<head>
    <style>
        .caixas {
            display: flex;
            flex-wrap: wrap;
        }

        .caixas > div {
            background-color: springgreen;
            font-size: 20px;
            margin: 20px;
            padding: 20px;
            width: 200px;
            height: 200px;
            font-family: monospace;
        }
    </style>
</head>
<body>
    <div class="caixas">
        <div>Primeira caixa</div>
        <div>Segunda caixa</div>
        <div>Terceira caixa</div>
        <div>Quarta caixa</div>
        <div>Quinta caixa</div>
        <div>Sexta caixa</div>
    </div>
</body>
```

Outro exemplo é caso se tenha uma tabela com o terceiro campo com espaço sobrando em torno da informação, queremos que esse espaço seja diminuido ou aumentado caso necessário.

```html
<head>
    <style>
        .tabela {
            background-color: darkgreen;
            display: grid;
            padding: 20px;
            grid-column-gap: 20px;
            grid-row-gap: 10px;
            grid-template-columns: 200px 200px auto;
        }

        .item_tabela {
            background-color: white;
            font-size: 15px;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="tabela">
        <div class="item_tabela">1</div>
        <div class="item_tabela">2</div>
        <div class="item_tabela">3</div>
        <div class="item_tabela">4</div>
        <div class="item_tabela">5</div>
        <div class="item_tabela">6</div>
        <div class="item_tabela">7</div>
        <div class="item_tabela">8</div>
        <div class="item_tabela">9</div>
    </div>
</body>
```

