

## ⋆˚✿˖° Actividad 4 ⋆˚✿˖°


``` sql
 with detenido_fecha as (
SELECT PAIS_PRISI__N as pais, G__NERO as sex
from `Is_2023_2.Colombianos_detenidos` CD
where (CD.FECHA_PUBLICACI__N between '2022-01-01' and '2022-12-31') )

SELECT DF.pais ,count (*) as Total
FROM detenido_fecha DF
WHERE DF.pais <> 'DESCONOCIDO'
GROUP BY DF.pais 
ORDER BY Total DESC LIMIT 10
sql
```
La consulta utiliza una subconsulta llamada **"detenido_fecha"**, que extrae la información relevante de la tabla **"Colombianos_detenidos"**. La subconsulta selecciona el país de prisión y el género de los detenidos cuya fecha de publicación se encuentra en el rango entre el 1 de enero de 2022 y el 31 de diciembre de 2022

La consulta principal realiza el recuento de detenidos por país y excluye aquellos casos donde el país es **"DESCONOCIDO"**. Luego, agrupa los resultados por país y los ordena en orden descendente según el recuento total. Por último, se limita la salida a los diez primeros resultados.

---
## Dashboard 
[LookerStudio.com](https://lookerstudio.google.com/reporting/d59af4ec-baae-4e27-a627-9c7113eb4bd8)