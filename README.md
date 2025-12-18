<div>
  <img style="100%" src="https://capsule-render.vercel.app/api?type=waving&height=100&section=header&reversal=false&fontSize=100&fontColor=FFFFFF&fontAlign=50&fontAlignY=50&stroke=-&desc=BACKEND%20FINAL&descSize=85&descAlign=50&descAlignY=50&color=gradient"  />
</div>

###

<p align="left">Creamos este proyecto, de cursos en donde aparecen los usuarios en el que podemos crearlos  y obtener información de los mismos y poder subirlos.</p>

###

<p align="left">Creamos un repositorio en GitHub para guardar los cambios que hagamos y agregar archivos y códigos, también creamos una base de datos en firebase  para relacionarlos en el proyecto.</p>

###

<p align="left">instalamos las librerías de fastApi, uvicorn, y firebase para poder usarlas en phyton y luego las guardamos en gtihub por la terminal de visual.</p>

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="vscode logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg" height="40" alt="firebase logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg" height="40" alt="fastapi logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="40" alt="github logo"  />
</div>

###

<p align="left">En el visual code creamos el repositorio en donde contiene el Archivo venv que contiene las dependencias de las librerías para que todo funcione correctamente .</p>

###

<p align="left">También esta el archivo gitignore en done ubicamos  los archivos que queremos ocultar las credenciales sin afectar su funcionamiento.</p>

###

<p align="left">El archivo firebase.json que creamos para relacionar la base de datos con phyton.</p>

###

<p align="left">El main.py donde se encuentra todos los códigos de phyton para ejecutar.</p>

###

<p align="left">Por ultimo el requirements.txt en el cual declaramos las librerías para su funcionamiento correcto</p>

###

<h2 align="left">Explicación del código.</h2>

###

<p align="left">1. Configuración de Firebase y FastAPI<br>El código comienza estableciendo la comunicación con la base de datos y creando la aplicación web.<br><br>credentials.Certificate("firebase.json"): Carga las llaves de acceso desde un archivo local para poder entrar a tu base de datos.<br><br>firestore.client(): Crea el objeto db, que es el que usaremos para leer o escribir datos.<br><br>app = FastAPI(): Crea la instancia de la aplicación que escuchará las peticiones en internet.<br><br>2. Estructura de los Datos (Modelos)<br>Se utilizan clases basadas en BaseModelpara definir qué información es obligatoria. Esto sirve para que, si alguien intenta enviar datos incompletos o erróneos, FastAPI lo rechace automáticamente.<br><br>Usuario: Defina que cada usuario debe tener nombre, edad, correo electrónico, contraseña y una repetición de la misma.<br><br>Curso: Defina que cada curso requiere nombre, descripción y duración.<br><br>3. Puntos finales (Rutas de la API)<br>El código define "rutas" para que los clientes (como una aplicación móvil o una página web) puedan interactuar con los datos.<br><br>Gestión de Usuarios<br>GET /usuarios: Entra a la colección de "usuarios" en la nube, descarga todos los documentos y los devuelve como una lista.<br><br>POST /usuarios: Recibe los datos de un nuevo usuario.<br><br>Validación: Revisa que contraseña == repetir_contraseña.<br><br>Limpieza: Elimina el campo repetir_contraseñaantes de guardar, para no ocupar espacio innecesario.<br><br>Guardado: Registra el usuario en la base de datos.<br><br>Gestión de Cursos<br>GET /cursos: Trae la lista de todos los cursos disponibles en la base de datos.<br><br>POST /cursos:Recibe un curso nuevo.<br><br>Validación: Tiene una regla que prohíbe crear cursos cuyo nombre sea "admin" (una medida de seguridad simple).<br><br>Guardado: Registra el curso en la colección correspondiente.<br><br>Salud del Sistema<br>GET /health: Una ruta simple que devuelve "hola" para verificar que el servidor está funcionando correctamente.</p>

###
