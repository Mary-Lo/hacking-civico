Se importan las liberias de pandas, numpy y statistics para poder manejar adecuadamente los datos.

Se importan las bases de datos del gobierno y se cargan en el cuaderno de python.

Después de la limpieza de datos se realiza una función para identificar el porcentaje de defunciones con hipertensión:

 `hipertension=datos.query('hipertension == "1" & fecha_def != 9999-99-99')`
 
 y luego el total de casos 
 
 `total=datos.query('fecha_def != 9999-99-99')`
 
 Y con esto se saca el porcentaje de personas difuntas que padecían hipertensión 
 
 Posterioremente con un query podemos filtrar los datos para ver el número de fallecidos diagnosticados con hipertensión y el número de personas con covid que siguen vivas 
 y también padecen hipertensión.
 
 Con un nuevo query filtramos lo datos para obtener el número de casos por municipio
 
 `municipios=casos.entidad_res.value_counts()`
 
 y hacemos lo mismo para el número de defunciones por municipio y los pacientes ambulantes
 
 `rip.entidad_res.value_counts()`
 
 `ambulatorios=datos.query('tipo_paciente == "1" & fecha_def != "9999-99-99"')`
 
  


