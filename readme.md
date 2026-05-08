### Proyecto Práctica 2026

Institución: Escuela Técnica N°1 Cnel. Manuel Alvarez Prado
Año: 2026
Autor: Nicolás Nicanor Gutierrez
Email: 38975442@populorumjujuy.ar
GitHub: NicoG95

- Definición del problema
  Actualmente el registro de asistencias de los alumnos se realiza mediante planillas físicas de papel. Este método genera una comunicación lenta entre los profesores de taller, profresores de educación física y preceptores de clases teóricas dificultando el seguimiento diario y la verificación de datos al finalizar cada jornada.

- Objetivo general
  Desarrollar un sistema de asistencia digital propio para la institución, o instituciones en general, que permita el registro de alumnos a través de los dispositivos móbiles del personal docente y administrativo.

- Objetivos específicos
  *Digitalización: eliminar el uso de planillas físicas para asistencia en talleres y aulas teóricas.
  *Optimización: agilizar la carga de datos de asistencia mediante un sistema móvil que sea intuitiva para profesores y preceptores.
  \*Integración: mejorar la comunicación interna entre personal administrativo (preceptores) y docentes a la hora de pasar lista y registrar asistencia.

- Beneficiarios
  *Personal docente y preceptores: menor carga administrativa y mayor facilidad para calcular y acceder a la situación de cada alumno en términos de inasistencias.
  *Alumnos y padres: mayor control y seguridad sobre la presencia escolar.

- Alcance del proyecto
  El sistema cubrirá la totalidad de los cursos de la Escuela Técnica N°1 abarcando su doble turno (teoría y talleres) y hasta, en algunos casos, triple asistencia diaria (algunos días de la semana el alumno tendrá educación física sumada a teoría y talleres) de cada alumno, permitiendo pasar lista y registrar la asistencia desde los teléfonos celulares tanto de preceptores como de profesores.

Cronograma de actividades
-Mes 1: definición + análisis
-Mes 2: Diseño UX/UI
-Mes 3: Arquitectura + base de datos
-Mes 4: Backend core
-Mes 5: Backend avanzado
-Mes 6: Desarrollo web
-Mes 7: app móvil
-Mes 8: Testing + deploy

Estudio de factibilidad
No se requieren equipos especiales, solo acceso a internet

Tecnica
Lenguajes: PHP + laravel, Flutter
Base de datos: MySQL
Dispositivos: teléfonos celulares, pc de escritorio

Economica
El proyecto tiene bajo costo ya que se utilizan herramientas de desarrollo gratuitas y no se requiere comprar hardware adicional.

Operativa
El sistema es operativamente viable ya que el personal ya utiliza teléfonos móviles.

Requerimientos Funcionales

Requisitos generales

- El sistema debe ser accesible desde dispositivos móviles.
- El sistema debe ser accesible desde una pc de escritorio a utilizar por el administrador.
- El sistema debe contar con conexión a internet.

Requisitos funcionales

El sistema debe permitir

- Registrar usuarios y sus roles
- Registrar alumnos y sus respectivos cursos y divisiones y asignarles preceptores.
- Registrar clases de taller y educación física y asignarle sus respectivos profesores.
- Registrar asistencia diaria tanto en clases teóricas como en taller y educación física.
- Modificar registros en casos de eror.
- Consultar historial de asistencias.
- Visualizar listados de alumnos por curso y división.
- Registrar múltiples asistencias en un mismo día.

### Script de cálculo de edad

Este script permite calcular la edad de una persona a partir de su año de nacimiento.

### Como ejecutarlo

1. tener visual studio code y python instalado
2. ejecutar en terminal
3. ingresar tu año de nacimiento.
4. ingresar el año actual.

### Diseño

- Modelo de datos: El sistema se plantea como una aplicación web y móvil que permite a docentes y preceptores registrar la asistencia de los alumnos, con frontend hecho en Flutter y backend hecho en Laravel, además de MySQL para la base de datos.
  1. Datos de entrada: Información de los alumnos (nombre, apellido, DNI, curso y división). Información de docentes y preceptores (nombre, rol, cursos y divisiones asignados, asignaturas de taller). Registro de asistencia diaria (fecha, asignatura, presente, ausente, tardanza, justificado).
  2. Datos internos: Tabla de usuarios, tabla de alumnos vinculada a cursos y divisiones, tabla de clases de taller vinculada a curso (año escolar) y grupo, relación entre alumnos y asistencia (historial).
  3. Datos de salida: reportes de asistencia por curso y división, listado de alumnos con cantidad de inasistencias acumuladas, notificaciones internas para el personal administrativo.

### Base de Datos

1. Tabla usuarios: id_usuario, nombre, rol, email, correo.
2. Tabla alumnos: id_alumno, nombre, apellido, curso, división.
3. Tabla clases: id_clase (teoria, taller, educación física), encargado_asistencia (prof. taller, prof. ed. física, preceptor) fecha.
4. Tabla asistencias: id_asistencia, id_alumno, id_clase, estado (presente, ausente, tardanza, justificado)

### Dependencias

1. Framework Laravel (PHP)
2. Flutter para app móvil y web
3. MySQL, motor de base de datos

### Software (herramientas)

1.  Visual Studio Code
2.  Git + GitHub
3.  Laragon, para servidor local
4.  Android Studio para pruebas móviles

### Procedimiento de instalación

1. Instalar dependecias de Laravel y Flutter
2. Configurar base de datos MySQL
3. Ejecutar migraciones.
4. Levantar servidor local con Laragon o Laravel Artisan

### Procedimientos de testing

1.  Pruebas en Laravel y Flutter
2.  Validación de roles y permisos.
3.  Carga de datos y generación de reportes.

### Git Branch-D
Función: Elimina una rama local de manera forzada

Sintaxis: git branch -D nombre_rama