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
