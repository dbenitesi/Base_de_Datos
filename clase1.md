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
