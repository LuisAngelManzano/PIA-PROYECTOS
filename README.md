# Universidad Autónoma de Nuevo León (UANL)
## Facultad de Contaduría Pública y Administración (FACPYA)
### Licenciatura en Tecnologías de la Información (LTI)

---

# ⏱️ PIA: Sistema de Gestión de Horas y Proyectos

**Participante Principal:** Luis Angel Manzano Cruz (Líder Técnico y Desarrollador Backend)  
**Equipo:** Proyecto desarrollado en colaboración académica.  
**Materia:** Gestión de Proyectos  
**Semestre:** Octavo Semestre  

---

## 📌 ¿De qué trata este proyecto?

Este sistema es una plataforma web creada para una **firma de asesoría financiera y fiscal**. **El problema:** Antes, la empresa llevaba el control de las horas que trabajaba cada empleado usando papel o archivos de Excel. Esto hacía muy difícil saber si un proyecto estaba consumiendo más horas de las presupuestadas y complicaba la generación de reportes.

**La solución:** Esta plataforma digitaliza todo el proceso. Permite registrar a los clientes, crear proyectos con un límite de horas, asignar a los trabajadores y llevar un control automático. Así, los jefes pueden ver en tiempo real si un proyecto es rentable y descargar reportes automáticos.

---

## 👥 ¿Qué puede hacer cada tipo de usuario?

El sistema está dividido en dos perfiles principales para mantener la información segura y organizada:

### 1. Perfil de Administrador (Gerentes o Jefes)
Es el encargado de configurar y vigilar todo el sistema. Sus herramientas principales son:
* **Catálogos:** Puede registrar, editar y dar de baja a nuevos *Clientes*, *Proyectos* y *Empleados*.
* **Asignación de trabajo:** Decide qué empleados participan en qué proyectos.
* **Control de Rentabilidad:** Tiene una pantalla especial que compara las "Horas Presupuestadas" (el límite del proyecto) contra las "Horas Registradas" (lo que realmente ha trabajado el equipo), calculando la diferencia al instante.
* **Reportes:** Puede buscar información por fechas, empleado o cliente, y exportar los resultados en documentos **PDF** o tablas de **Excel** para presentarlos en juntas.

### 2. Perfil de Empleado (Trabajadores)
Es una pantalla más sencilla, diseñada solo para que el trabajador reporte su día a día sin complicaciones.
* **Seguridad personal:** Al entrar por primera vez, el sistema le exige cambiar la contraseña temporal que le dio el administrador por una clave personal.
* **Registro de horas:** Puede seleccionar un proyecto, elegir la fecha, anotar cuántas horas dedicó y describir qué hizo. El sistema lo protege de errores (por ejemplo, no lo deja registrar horas en fechas del futuro o en proyectos en los que no participa).
* **Su historial:** Puede consultar en cualquier momento la lista de todas las horas que ha reportado en el pasado.

---

## 🚀 Guía rápida de uso (Paso a paso)

Si es la primera vez que se usa el sistema, este es el orden correcto para configurarlo:

1. **Crear un Cliente:** Ir al panel de administrador y registrar los datos de la empresa a la que se le va a trabajar (Nombre, RFC, correo).
2. **Crear un Empleado:** Llenar el formulario con los datos del trabajador. El sistema creará un "Nombre de Usuario" automático y el administrador le asignará una contraseña temporal.
3. **Crear un Proyecto:** Ponerle un nombre, elegir las fechas de inicio/fin, definir cuántas horas en total va a durar el proyecto y asignarlo al cliente que creamos en el paso 1.
4. **Asignar el Proyecto:** Ir a la lista de empleados y vincular al trabajador con el proyecto que acabamos de crear.
5. **Registrar Horas:** Ahora el empleado entra a su cuenta, cambia su contraseña temporal, selecciona el proyecto y guarda las horas que trabajó hoy.
6. **Revisar Reportes:** El administrador puede entrar a la sección de reportes, ver las horas que subió el empleado y descargar el PDF con el resumen.

---

## 🛠️ Herramientas utilizadas para construirlo

* **Lenguaje principal:** Python
* **Estructura del sitio (Framework):** Django
* **Base de datos:** SQLite (ideal para el desarrollo local)
* **Diseño visual:** HTML, CSS y JavaScript

---

## 📖 Documentación Visual
Para conocer a detalle el flujo de la aplicación, las reglas de negocio y ver capturas de pantalla de las interfaces de usuario, puedes consultar el manual oficial del sistema:
👉 **[Ver Manual de Usuario y Administrador](./docs/MANUAL_IMPRESION.pdf)**

---

## ⚙️ ¿Cómo probar el proyecto en tu computadora?

Si el profesor o evaluador desea encender el sistema en su propia máquina local, solo necesita seguir estos pasos en la terminal (Git Bash o PowerShell):

**1. Descargar la carpeta del proyecto**
```bash
git clone [https://github.com/LuisAngelManzano/PIA-PROYECTOS](https://github.com/LuisAngelManzano/PIA-PROYECTOS.git)
cd PIA-PROYECTOS

-python -m venv env
.\env\Scripts\activate
-pip install -r requirements.txt
-python manage.py migrate
-python manage.py runserver
Una vez encendido, abre tu navegador de internet y entra a la dirección: http://127.0.0.1:8000/
