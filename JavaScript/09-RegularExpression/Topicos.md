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

> <font color="lightgreen"> \+ * ? ^ $ . [ ] { } ( ) | \ / </font>
 
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

  - **\\**: Forma de scape, seleciona **realmente o valor** ao invez do tipo especial. Exemplo: **/ \ . /** 
    ```javascript
    EXEMPLO
    ```

  - **[]** (no meio): seleciona entre **um ou outro** caracter. 
    ```javascript
    EXEMPLO
    ```

 - **-**: Dentro de **[]** serve para definir um alcance. (Tabela Unicode)
    ```javascript
    EXEMPLO
    ```

- **^**: dentro de **[]** serve para negar o caracter que vem seguido.
    ```javascript
    EXEMPLO
    ```

## Words


 ### Mais utilizadas

  - **\w**: Seleciona caracterens alfaNuméricos e o underline. ex: [A-Za-z0-9_]
    ```javascript
    EXEMPLO
    ```

 - **\d**: Seleciona tudo que é caracter numerico. ex: [0-9].
 - **\D**: tudo que não é digito, letras, espaços, etc.
 - **\s**: Seleciona tudo que é espaço, quebra de linha e tabs.
 - **\S**: Seleciona tudo que não é espaço, etc.
 - **+**: Seleciona uma ou mais ocorrencias como unica para o caracter antecessor a ele.
- **\***: Faz o caracter antecessor se tornar opcional, ocorrencia de 0 ou mais.
- **?**: Faz o caracter antecessor se tornar opcional, ocorrencia de 0 ou mais.
- **|**: Seleciona um ou outro.
- **^**: Linha inicia com a ocorrencia seguinte.
- **$**: Linha final com a ocorrencia anterior.
- **\u**: indica o unicode especifico que deseja selecionar.


## Funções especiais para substituição

###Mais utilizados

 - **$&**: Referencia a palavra selecionada no Regex.
 - **( )**: Cria grupos de seleção para dividir o Regex selecionado.
 - **(?=)**: Seleciona o antecessor que contenha a informação infomada apos o ?=.



 ## Padroes Conhecidos.
Cep
 ```JavaScript 
    regex: /\d{5}[\s-]?\d{3}/g
    /*
        00000-000
        00000 000
        00000000
    */
 ```   
 CPF
 ```javascript
Regex: /(?:\d{3}[\s-|.]?){3}\d{2}/g
    /*
        000.000.000-00
        000-000-000-00
        000.000.000.00
        000000000-00
        00000000000
        000 000 000 00
    */
 ```
 CNPJ
 ```javascript
Regex: /\d{2}[-.\s]?(\d{3}[-.\/\s]?){2}\d{4}[-.\s]?\d{2}/g
    /*
        00.000.000/0000-00
        00000000000000
        00-000-000-0000-00
        00.000.000.0000.00
        00 000 000 0000 00
    */

 ```
 Email
 ```javascript
Regex: /[\w.-]+@[\w-]+\.[\w-.]+/gi
    /*
        email@email.com
        email@email.com.org
        email-enauk@email.com.br
        email_eamaw@email.com
        email.emaema123@email.com
        email.emae12@empresa-sua.com.br
        c@contato.cc
    */
 ```
---
## Metodos de Regex


###Construtor
```JavaScript
const regexp = /\w+/gi;
/*
 * Se passarmos uma string, não precisamos dos //
 * e devemos utilizar \\ para meta characteres, pois é necessario
 * escapar a \ especial, As Flags são o segundo argumento,
*/
const regexObj1 = new RegExp('\\w+', 'i'); 
const regexObj2 = new RegExp(/\w+/, 'i'); 
```