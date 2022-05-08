# laravel
software de cafeteria


Utilizar un servidor para lanzar el proyecto.
Utilizar postman o insomnia para recoger los distintos datos.
Utilizar el comando de  php artisan route:list para visualizar todas las rutas.

Anexo las consultas de mysql:

Realizar una consulta que permita conocer cuál es el producto que más stock tiene:
SELECT * FROM products WHERE stock in (select MAX(stock) from products)

Realizar una consulta que permita conocer cuál es el producto más vendido:
SELECT * FROM products WHERE id IN (SELECT product_id FROM orders WHERE quantity IN (SELECT MAX(quantity) FROM orders))
