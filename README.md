# ⚖️ Arbitraje ACIR - Sistema de Gestión de Casos Arbitrales

Este proyecto es una propuesta de solución web desarrollada con **React** y **Firebase**, enfocada en mejorar la eficiencia del proceso de arbitraje en la empresa **ACIR Internacional**.

---

## 🚀 Descripción del Proyecto

**Arbitraje ACIR** es una aplicación web que permite a tres tipos de usuarios interactuar con el sistema de forma segura:

- 👤 **Clientes:** pueden registrar sus casos, subir documentación y dar seguimiento a sus expedientes.
- 🧑‍⚖️ **Árbitros:** pueden gestionar los casos asignados y emitir observaciones.
- 🛠️ **Administradores:** controlan todo el flujo de trabajo, revisan expedientes, agregan árbitros y verifican documentación.

---

## 🎯 Funcionalidades Principales

- ✅ Autenticación y autorización por roles (cliente, árbitro, admin)  
- ✅ Mesa de Partes Virtual (registro de casos y carga de documentos)  
- ✅ Gestión de árbitros y casos  
- ✅ Seguimiento del estado del caso  
- ✅ Visualización y descarga de expedientes (solo para administradores)  
- ✅ Interfaz moderna y responsiva con **MUI (Material UI)**  

---

## ⚙️ Tecnologías Utilizadas

| Herramienta | Uso |
|------------|-----|
| ![React](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=white&style=flat-square) | Construcción de la interfaz |
| ![Firebase](https://img.shields.io/badge/-Firebase-FFCA28?logo=firebase&logoColor=white&style=flat-square) | Backend completo (auth, db, storage) |
| ![MUI](https://img.shields.io/badge/-MUI-007FFF?logo=mui&logoColor=white&style=flat-square) | Componentes UI accesibles y elegantes |
| ![React Router](https://img.shields.io/badge/-React%20Router-CA4245?logo=reactrouter&logoColor=white&style=flat-square) | Navegación entre vistas |

---

## 🧠 Estructura del Proyecto

```plaintext
src/
│
├── assets/         # Imágenes y recursos estáticos
├── components/     # Componentes reutilizables (Navbar, Sidebar, etc.)
├── firebase/       # Configuración de Firebase y funciones de auth/db
├── hooks/          # Custom hooks como useAuth
├── layouts/        # Layouts principales por tipo de usuario
├── pages/          # Páginas principales por rol
│   ├── Admin/
│   ├── Client/
│   └── Arbitrator/
├── routes/         # Configuración de rutas protegidas por rol
├── services/       # Funciones de interacción con Firestore y Storage
├── styles/         # Estilos globales
└── App.jsx         # Enrutamiento general y contextos
