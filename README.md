# Arbitraje ACIR - Sistema de Gestión de Casos Arbitrales

Este proyecto es una propuesta de solución web desarrollada con **React** y **Firebase**, enfocada en mejorar la eficiencia del proceso de arbitraje en la empresa **ACIR Internacional**.

---

## 🚀 Descripción del Proyecto

**Arbitraje ACIR** es una aplicación web que permite a tres tipos de usuarios interactuar con el sistema de forma segura:

- **Clientes:** pueden registrar sus casos, subir documentación, dar seguimiento a sus expedientes.
- **Árbitros:** pueden gestionar los casos que se les asignan y emitir observaciones.
- **Administradores:** controlan todo el flujo de trabajo, revisan expedientes, agregan árbitros y verifican documentación.

---

## 🎯 Funcionalidades Principales

- ✅ Autenticación y autorización por roles (cliente, árbitro, admin)
- ✅ Mesa de Partes Virtual (registro de casos y carga de documentos)
- ✅ Gestión de árbitros y casos
- ✅ Seguimiento del estado del caso
- ✅ Visualización y descarga de expedientes (solo para administradores)
- ✅ Interfaz moderna y responsiva con MUI (Material UI)

---

## ⚙️ Tecnologías Utilizadas

| Herramienta | Uso |
|------------|-----|
| React.js | Construcción de la interfaz |
| Firebase Auth | Autenticación de usuarios |
| Firebase Firestore | Base de datos en tiempo real |
| Firebase Storage | Subida y gestión de archivos |
| MUI | Componentes UI accesibles y elegantes |
| React Router | Navegación entre vistas |

---

## 🧠 Estructura del Proyecto (React + Firebase)

src/
│
├── assets/ # Imágenes y recursos estáticos
├── components/ # Componentes reutilizables (Navbar, Sidebar, etc.)
├── firebase/ # Configuración de Firebase y funciones de auth/db
├── hooks/ # Custom hooks como useAuth
├── layouts/ # Layouts principales por tipo de usuario
├── pages/ # Páginas principales por rol
│ ├── Admin/
│ ├── Client/
│ └── Arbitrator/
├── routes/ # Configuración de rutas protegidas por rol
├── services/ # Funciones de interacción con Firestore y Storage
├── styles/ # Estilos globales
└── App.jsx # Enrutamiento general y contextos


---

## 🧩 Estructura de la Base de Datos (Firestore)

```plaintext
users (colección)
 └── userId
      ├── name
      ├── email
      ├── role: 'admin' | 'client' | 'arbitrator'

cases (colección)
 └── caseId
      ├── clientId
      ├── title
      ├── description
      ├── status: 'En revisión' | 'En proceso' | 'Finalizado'
      ├── arbitratorId
      ├── expedienteUrl
      └── timestamps

documents (colección)
 └── docId
      ├── caseId
      ├── uploadedBy
      ├── url
      ├── name
      └── createdAt

📌 Consideraciones de Seguridad

    🔐 Se protege el acceso a la información con Firebase Rules y validación por roles.

    🔐 Solo los administradores pueden acceder a los expedientes completos.

    🔐 Clientes y árbitros solo ven los casos relacionados a su cuenta.

🌱 ¿Por qué este proyecto?

Esta propuesta busca demostrar mi capacidad para:

    Aplicar buenas prácticas de desarrollo frontend con React.

    Integrar Firebase para auth, database y storage.

    Pensar en flujos reales de negocio como los de una empresa de arbitraje.

    Crear una solución funcional, escalable y segura.

👨‍💻 Autor

Ángel “Vitio” Quijano
GitHub | LinkedIn
Desarrollador web apasionado por resolver problemas reales con tecnología.
