# Modelos bases de datos
Bienvenidos al repositorio del curso de modelos de bases de datos. Aquí encontrarás recursos necesarios para los ejercicios.

1. entra a github.com/polizona/modelos

2. descarga los scripts de carga para las tablas de embarques y financieras

3. entra a tu base de datos

4. ejecuta los scripts de carga

5. escribe una consulta a la tabla embarques que despliegue boleta, idinsumo y calcule el costo promedio por insumo 


select materia, industria, financieras.boleta, idinsumo, sum(unidades*costoUnitario)/sum(unidades) from embarques, financieras where financieras.boleta=embarques.boleta group by boleta, idinsumo order by materia, industria, boleta, idinsumo
