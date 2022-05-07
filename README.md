# php-mysql
Usem como referência a implemtação do https://github.com/wistech7l/Crud_Concessionaria

# Passos
Criar as páginas php com Html, se quiserem criarem a estilização com CSS fiquem a vontade. 
Também se quiserem reutilizar o modelo do php-login que fizemos anteriormente também pode.

## 1 Criar banco de dados
## 1.1 Criar uma tabela 
(sugestão)
|| filmes|||
|---| --- | --- | --- |
|colunas| id | nome | ano |
|Propriedades|int, auto incremental, not null, chave primária| string(50), not null | int, not null |

## Páginas PHP ( usando o html dentro do php )
1) Criem uma página index 
2) Criem uma página para listar: no comando de repetição já podemos definir nosso objeto 

Ex.:  
```php
<?php
   for($i = 0; $i < count($filmes); $i++){
      echo '<tr>';
      echo '<td>'. $filmes[$i]['id'] .'</td>';
      echo '<td>'. $filmes[$i]['nome'] .'</td>';
      echo '<td>'. $filmes[$i]['ano'] .'</td>';
      echo '</tr>';
   }
?>

```

## Criar a conexão Php com o banco de dados 
1) Criar o arquivo que irá conter as funções
2) Criar a função de conectar com o banco de dados [Referência PHP](https://www.php.net/manual/pt_BR/mysqli.construct.php)
3) Criar a função para listar [ [1] referência PHP ](https://www.php.net/manual/pt_BR/mysqli.query.php), [ [2] referência PHP ](https://www.php.net/manual/pt_BR/mysqli-result.fetch-row.php), 
semelhante a [essa aqui que criamos em aula](https://github.com/wistech7l/Crud_Concessionaria/blob/dbff170539f268686158373ea3f1e0e2e66e7947/lib/mysql.php#L17-L38)
