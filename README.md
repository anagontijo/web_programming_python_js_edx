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
