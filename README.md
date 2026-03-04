# 📋 Gestor de Tareas CLI

Aplicación de línea de comandos para gestionar tareas personales con prioridades, fechas de vencimiento y persistencia en JSON. Sin dependencias externas.

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-brightgreen?style=flat)
![CLI](https://img.shields.io/badge/interfaz-CLI-black?style=flat)
![License](https://img.shields.io/badge/license-MIT-green?style=flat)

---

## 📌 ¿Qué hace este proyecto?

- Agregar tareas con prioridad (alta / media / baja) y fecha límite
- Listar tareas filtradas por estado (todas / pendientes / completadas)
- Marcar tareas como completadas o eliminarlas
- Detectar automáticamente tareas **vencidas**
- Guardar todo en `tareas.json` de forma persistente

---

## 🖥️ Demo

```
$ python task_manager.py listar

📋 Tareas (todas) — 3 encontradas

⏰ [a1b2c3d4] Estudiar Python (alta) | Límite: 2024-12-31 [VENCIDA]
⬜ [e5f6g7h8] Hacer portfolio (media) | Límite: 2025-01-15
✅ [i9j0k1l2] Subir proyectos a GitHub (baja)
```

---

## 🛠️ Tecnologías

| Módulo | Uso |
|---|---|
| `argparse` | Interfaz CLI con subcomandos |
| `json` | Persistencia de datos |
| `uuid` | Generación de IDs únicos |
| `datetime` | Control de fechas y vencimientos |

> ✅ Usa únicamente la **librería estándar de Python** — no requiere `pip install`

---

## 🚀 Instalación y uso

### 1. Clona el repositorio
```bash
git clone https://github.com/TU-USUARIO/gestor-tareas-cli.git
cd gestor-tareas-cli
```

### 2. Ejecuta directamente (sin instalar nada)
```bash
# Ver ayuda
python task_manager.py --help

# Agregar una tarea
python task_manager.py agregar "Estudiar Python" --prioridad alta --fecha 2025-12-31

# Listar tareas
python task_manager.py listar
python task_manager.py listar --filtro pendientes
python task_manager.py listar --filtro completadas

# Completar una tarea (usar el ID que aparece al listar)
python task_manager.py completar a1b2c3d4

# Eliminar una tarea
python task_manager.py eliminar a1b2c3d4
```

---

## 📂 Estructura del proyecto

```
gestor-tareas-cli/
├── task_manager.py  # Script principal
├── tareas.json      # Generado automáticamente (ignorado por Git)
├── .gitignore
└── README.md
```

---

## 💡 Posibles mejoras

- [ ] Exportar tareas a PDF o CSV
- [ ] Notificaciones de tareas próximas a vencer
- [ ] Interfaz visual en terminal con la librería `rich`
- [ ] Sincronización con Google Calendar

---

## 👤 Autor

**Luis Garro**
- GitHub: [@tu-usuario](https://github.com/YehiizonGCh)