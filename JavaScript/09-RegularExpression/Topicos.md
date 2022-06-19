#Regular Expression

 - Funciona como um buscador de Caracteres unicos.

```javascript
// Procura: a ( o primeiro)
const padraoRegex = /a/
```
---
## Flags

 - Modifica o formato de busca da Regex
 - Sempre ao final da Regex

 ### Mais utilizadas

  - g: **Procura todas as ocorrencias** de caracteres informados no Regex.  
    ```javascript
    EXEMPLO
    ```



  - i: **Ignora** sensitive key.  
    ```javascript
    EXEMPLO
    ```


---
## Character Class e Especiais

> {c:green}\+ * ? ^ $ . [ ] { } ( ) | \ / {/c}
 
 Caracteres nao alfa-numericos dentro da classe (regex)
 ### Mais utilizadas

  - []: Procura todas as ocorrencias **separadamente**.  
    ```javascript
    EXEMPLO
    ```


  - .: Seleciona **cada um** dos caracteres, todos.  
    ```javascript
    EXEMPLO
    ```


  - \: Forma de scape, seleciona **realmente o valor** ao invez do tipo especial. Exemplo: **/ \ . /** 
    ```javascript
    EXEMPLO
    ```

  - [] (no meio): seleciona entre **um ou outro** caracter. 
    ```javascript
    EXEMPLO
    ```

 - -: Dentro de **[]** serve para definir um alcance. (Tabela Unicode)
    ```javascript
    EXEMPLO
    ```

- ^: dentro de **[]** serve para negar o caracter que vem seguido.
    ```javascript
    EXEMPLO
    ```


