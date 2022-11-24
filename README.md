# BBDD-CodoACodo
Desafío BBDD

2) Realizar las siguientes consultas:

2.1 obtener los apellidos de los empleados.
SELECT apellido FROM empleado;

2.2 obtener los apellidos de los empleados sin repeticiones.
SELECT DISTINCT apellido FROM empleado;

2.3 obtener los datos de los empleados que tengan el apellido Lopez.
SELECT * FROM empleado AS e WHERE e.apellidos="Lopez";

2.4 obtener los datos de los empleados que tengan el apellido Lopez y los que tengan apellido Perez.
SELECT * FROM empleado AS e WHERE e.apellidos="Lopez" OR e.apellidos="Perez"

2.5 Obtener todos los datos de los empleados que trabajen en el departamento 14.
SELECT * FROM empleado AS e WHERE e.departamento_id=14;

2.6 Obtener todos los datos de los empleados que trabajen en el departamento 37 y 77.
SELECT * FROM empleado AS e WHERE e.departamento_id=37 OR e.departamento_id=77;

2.7 Obtener los datos de los empleados cuyo apellido comience con P.
SELECT * FROM empleado AS e WHERE e.apellido LIKE 'P%';

2.8 Obtener el presupuesto total de todos los departamentos.
SELECT SUM(presupuesto) FROM departamento;

2.9 Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado
y de su departamento.
SELECT e.nombre, e.apellidos,e.dni,d.nombre As área,d.presupuesto FROM empleado AS e INNER JOIN departamento AS d ON e.departamento_id=d.id;
