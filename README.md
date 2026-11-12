# CodeBites - Backend API & Real-Time Server

Backend RESTful e server WebSocket per la piattaforma **CodeBites**, sviluppato in Node.js ed Express per l'esame di Programmazione Web presso il **Politecnico di Bari**.

🔗 **Live App (Frontend):** [https://codebites-frontend2.onrender.com](https://codebites-frontend2.onrender.com)  
💻 **Repository Frontend:** [CodeBites_frontend2](https://github.com/gdesimini/CodeBites_frontend2)

## Architettura & Stack Tecnologico
- **Runtime & Framework:** Node.js, Express
- **Database:** MongoDB con ODM Mongoose (`models/`)
- **Sicurezza & Autenticazione:** JWT (JSON Web Token) su cookie `HTTP-only`, hashing password con `bcrypt`, middleware di verifica (`middleware/`)
- **Real-Time:** Socket.io (`socket.js`) per la sincronizzazione istantanea dei dati tra client connessi
- **Deploy:** Render

## Struttura del Progetto
- `controllers/` — Logica applicativa per gestione utenti e operazioni CRUD sulle ricette
- `routes/` — Definizione degli endpoint REST (`/api/users`, `/api/recipes`)
- `models/` — Schemi dati Mongoose (Utenti e Ricette)
- `middleware/` — Autenticazione JWT e protezione delle rotte private
- `socket.js` — Configurazione server WebSocket e gestione eventi real-time
- `server.js` — Entry point, configurazione CORS e connessione a MongoDB Atlas
