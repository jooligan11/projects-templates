# projects-templates
Repositorio de plantillas técnicas para proyectos Flask, Docker y AWS. Incluye estructuras base listas para reutilizar en despliegues con EC2, RDS, Nginx, Gunicorn y arquitecturas de red en AWS. Diseñado para estandarizar proyectos, acelerar despliegues y mantener buenas prácticas de IT Ops y DevOps.
📁 Plantillas incluidas
1️⃣ portal_login_aws
Plantilla base para un portal de login en Flask desplegado en AWS EC2, conectado a RDS MySQL, usando Gunicorn como servidor WSGI y Nginx como proxy inverso.
📂 Estructura de carpetas de la plantilla
portal_login_aws/
├── login_ssr.py               # Aplicación Flask principal (Server-Side Rendering)
├── requirements.txt           # Dependencias del proyecto
├── README.md                  # Documentación específica de la plantilla
├── .gitignore                 # Archivos ignorados por Git
├── .env.example               # Variables de entorno de ejemplo
│
├── templates/                 # Plantillas HTML renderizadas por Flask
│   └── login.html             # Página de login
│
├── static/                    # Archivos estáticos (CSS, JS, imágenes)
│   ├── css/
│   └── js/
│
├── nginx.conf                 # Configuración de Nginx para proxy inverso
│
└── systemd/                   # Servicios del sistema para EC2
    └── loginapp.service       # Servicio systemd para Gunicorn
