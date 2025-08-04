# Como resolver o problema Drop Foreign Key
## 1. 🔍 Descubra o nome da constraint
Execute:
```
sql
SHOW CREATE TABLE sua_tabela;
````
### Procure por algo como:
```
CONSTRAINT nome_da_constraint FOREIGN KEY (coluna) REFERENCES outra_tabela(id)
```
## 2. 🧹 Remova a chave estrangeira
Use o nome da constraint para removê-la:

```
ALTER TABLE sua_tabela DROP FOREIGN KEY nome_da_constraint;
```

## 3. 🧼 Remova o índice (se necessário)
Às vezes, a chave estrangeira cria um índice. Remova com:

``` 
ALTER TABLE sua_tabela DROP INDEX nome_do_indice;

```
## 4. 🧨 Agora sim, apague a coluna
```
ALTER TABLE sua_tabela DROP COLUMN nome_da_coluna;
```
