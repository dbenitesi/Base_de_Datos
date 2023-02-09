<h1><strong>Escriba las consultas SQL solicitadas en los siguientes enunciados</strong></h1>
<br><p><strong>1.-</strong>Presentar las colimnas id, librospublicados, ademas en una sola colimna con nombre de cabecera nombre_completo el nombre, apellido1 y apellido }2 de forma concatenada</p>
<ul><li>SELECT autor.id, autor.librospublicados, concat(autor.nombre, " ", ifnull(autor.apellido1,""),ifnull(autor.apellido2,"")) as Nombre_Completo FROM autor;</li></ul>
<h1>Haga la seleccion y suma de libros publicados</h1>
<p>SELECT SUM(autor.librospublicados) as Suma_Libros_Publicados FROM `autor`;</p>
<h1>3.- Mostrar una consulta con titulo de libroo, nombre de la categoria a la que pertenece cada libro, mostrar solo los libros del autor J.K ROULING.</h1>
<p>SELECT libro.titulo, categoria.nombre 
FROM categoria, libro, autor 
WHERE autor.id = 4
AND libro.idautor = autor.id AND categoria.id = libro.idcategoria</p>
<h1>Mostrar una consulta de los libros y el estado de la categoria a la que pertenece 

<p>SELECT libro.titulo, libro.id, autor.nombre as autor, autor.librospublicados, categoria.nombre as categoria, editorial.nombre as editorial, sexo.descripcion as sexo
from autor
LEFT JOIN sexo on autor.idsexo = sexo.id
RIGHT JOIN libro on libro.idautor = autor.id
LEFT JOIN categoria on libro.idcategoria = categoria.id
LEFT JOIN editorial on libro.ideditorial = editorial.id;
  </p>
<p>SELECT libro.titulo, CONCAT(autor.nombre, autor.apellido1, autor.apellido2) AS NombreAutor, sexo.descripcion as sexo,  categoria.nombre as categoria, editorial.nombre as editorial
from autor 
LEFT JOIN sexo on autor.idsexo = sexo.id 
RIGHT JOIN libro on libro.idautor = autor.id 
LEFT JOIN categoria on libro.idcategoria = categoria.id 
LEFT JOIN editorial on libro.ideditorial = editorial.id
WHERE categoria.estado = 1
  order BY categoria.nombre</p>

  
