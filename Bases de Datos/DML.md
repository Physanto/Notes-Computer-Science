

Se encarga de realizar diferentes operaciones a los datos que se encuentran en la base de datos.

## Sentencias definidas para DML

- ==INSERT==: Se utiliza para la inserción de datos.
- ==SElECT==: Se utiliza para buscar registros.
- ==UPDATE==: se usa para actualizar un registro especifico dependiendo su condición.
- ==DELETE==: Se usa para eliminar un registro dependiendo su condicion.

```mysql
INSERT INTO nombre_tabla
	(columna1, columna2, columna3),	
	VALUES
	(valor_columna1, valor_columna2, valor_columna3);

```

```mysql
SELECT columna1, columna2, columna3... FROM nombre_tabla
```

```mysql
SELECT * FROM nombre_tabla

#* representa todas las columnas
```

```mysql
UPDATE nombre_tabla
SET columna1=nuevo_valor_columna1, columna2=nuevo_valor_columna2...
WHERE condicion;
```

```mysql
DELETE FROM nombre_tabla
WHERE condicion;
```


- ON DELETE Y ON UPDATE: Nos permiten indicar el efecto que provoca el borrado o la actualizacion de los datos que estan referenciados por claves ajenas. 

existen opciones que podemos especificar cuando podemos borrar o actualizar

- ==RESTRICT==: Impide que se puedan eliminar o actualizar los registros.
- ==CASCADE==: Cuando se da la orden de manipular un registro la actualizacion o eliminacion modifica donde apunta la llave que referencia.
- ==SET NULL==:
- ==NO ACTION==:
- ==SET DEFAULT==: hace que se le ponga un valor determinado en donde el elemento se encuentra referenciado.
