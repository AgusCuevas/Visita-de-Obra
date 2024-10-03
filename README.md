# Visita-de-Obra
Una empresa constructora quiere manejar de forma centralizada los informes de visita de obra
de sus especialistas de seguridad e higiene. Un arquitecto carga carga planos de obra,
planificación de la obra, notas y solicitar a uno o varios inspectores que realicen una visita de
obra.

# SITUACION ACTUAL
Actualmente no hay ningún sistema para la visita de obra. Un arquitecto lleva en una carpeta
planos de obra, planificación de la obra, notas y cuando lo requiere envía a un inspector al sitio
con una serie de indicaciones y copia de la documentación del sitio. El inspector recauda la
información en forma de notas que toma en forma manual y fotografías. Finalmente redacta un
informe en Word que envía vía mail al arquitecto de la obra. Los inspectores trabajan de forma
independiente y cobran por cada visita de obra. A fin de mes el arquitecto informa al sector de
pago a proveedores las visitas por inspector y se realiza el pago correspondiente.

# REQUERIMIENTOS
## Arquitectos 
- Poder cargar de ante mano los planos de los sitios, 
- Solicitud de inspección de sitio con verificaciones a realizar y la asignación de inspectores 
- Poder acceder a los informas de obra completados
## Inspectores / Seguridad e Higiene 
- Puedan dejar el informe en estado borrador hasta poder completarlo. 
- Puedan cargar fotos, notas y coordenadas GPS desde el sitio mediante su celular o tablet Android 
- No todas las sitios tienen buena conexión , la aplicación debe poder almacenar la información recolectada por los inspectores y sincronizarla cuando tenga conexión estable 
- Los inspectores pueden confeccionar el informe de visita de obra (complementado por la información recabada en el sitio) desde una PC , tables o celular. 
- Recibir notificaciones de visita de obra asignada
## Pago a proveedores 
- Ver informe de visitas de obra finalizadas

# TAREAS
Proponga una arquitectura que cumpla con los requerimientos antes mencionados
especificando
- A. Identifique sub-dominios (10 puntos) 
- B. Diagrama estructural de contenedores según el estándar C4 (30 puntos) 
- C. Decisiones de arquitectura de cada sub dominio (30 puntos) 
## EXTRAS (DEBE TENER LOS PUNTOS A, B y C completos) 
- D. Diagrama de estados de un informe de visita de obra (15 PUNTOS) 
- E. Diagrama de secuencia de asignación de visita de obra (15 PUNTOS)

# Solucion
## A. Identifique sub-dominios (10 puntos) 
- Sistema para arquitectos: Este subdominio permite a los arquitectos cargar planos, planificaciones, notas y asignar inspectores.
- Sistema para inspectores: Los inspectores acceden a las asignaciones, registran información (fotos, coordenadas, notas) y generan informes de visita de obra.
- Sistema para pagos: Gestiona el seguimiento y procesamiento de los pagos a los inspectores una vez completada la visita de obra.

## B. Diagrama estructural de contenedores según el estándar C4 (30 puntos) 
![image](https://github.com/user-attachments/assets/a3d05644-5b70-400b-9a89-7a3e169dd308)

## C. Decisiones de arquitectura de cada sub dominio (30 puntos) 
Arquitectura por capas: Se elige este patrón por su flexibilidad y capacidad de escalar. Se utilizara una interfaz de usuario multiplataforma (PC, tablets, móviles).
- Capa de presentación (UI): Aplicación web y móvil para todos los usuarios (arquitectos, inspectores, responsables de pago).
- Capa de lógica de negocio (Business): Maneja la lógica relacionada con las asignaciones, creación de informes, validaciones y pagos.
- Capa de acceso a datos: Permite operaciones de lectura/escritura en la base de datos.
- Capa de Base de datos: Almacena los datos de usuarios, asignaciones y visitas de obra.

## D. Diagrama de estados de un informe de visita de obra (15 PUNTOS) 
## E. Diagrama de secuencia de asignación de visita de obra (15 PUNTOS)
