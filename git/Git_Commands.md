## 🔧 Comandos Específicos de Git: Para Situaciones Particulares y Optimización
Estos comandos son útiles en escenarios más avanzados, como cuando necesitas reescribir el historial, resolver conflictos o mejorar la organización del código.

- **`git stash`**: 🛅 Guarda los cambios temporales sin hacer commit y limpia el área de trabajo.
- **`git stash apply`**: 🔙 Aplica los cambios guardados con `git stash`.
- **`git rebase <rama>`**: ♻️ Reorganiza los commits de una rama aplicándolos sobre otra. Útil para mantener un historial limpio, pero requiere precaución en equipos.
- **`git cherry-pick <hash>`**: 🍒 Aplica un commit específico de una rama a la rama actual.
- **`git reset --hard <hash>`**: ⏪ Restablece el repositorio al estado de un commit específico. Destruye los cambios no comprometidos.
- **`git reset --soft <hash>`**: 🧶 Restablece al estado de un commit, pero mantiene los cambios en el área de preparación.
- **`git revert <hash>`**: ⏮️ Crea un nuevo commit que revierte un commit específico.
- **`git fetch`**: 📡 Trae los cambios del repositorio remoto, pero no los integra automáticamente.
- **`git remote add <nombre> <url>`**: 🌐 Conecta tu repositorio local a un repositorio remoto.
- **`git diff`**: 🔍 Muestra las diferencias entre archivos no comprometidos y el último commit.
- **`git tag <nombre>`**: 🏷️ Crea una etiqueta en un commit específico para marcar una versión.
- **`git blame <archivo>`**: 👁️ Muestra quién modificó cada línea de un archivo, útil para rastrear cambios.
- **`git log --oneline --graph`**: 📊 Muestra un historial de commits simplificado y en forma de grafo para visualizar las ramas y merges.
- **`git reflog`**: 🗂️ Muestra un historial de todas las referencias a movimientos en el repositorio, útil para recuperar commits eliminados.
- **`git clean -fd`**: 🧹 Elimina archivos no rastreados (útil para limpiar el directorio de trabajo).

## 🚀 Comandos Esenciales de Git: Los Imprescindibles para Sobrevivir
Estos comandos son básicos y te permiten hacer el trabajo más común en Git, desde trabajar localmente hasta compartir tus cambios.

- **`git init`**: 🆕 Inicializa un repositorio de Git en un directorio.
- **`git clone <url>`**: 📥 Clona un repositorio remoto a tu máquina.
- **`git status`**: 🧐 Muestra el estado actual de tu repositorio (cambios pendientes, archivos no rastreados, etc.).
- **`git add <archivo>`**: ➕ Agrega archivos al área de preparación (staging).
- **`git commit -m "mensaje"`**: 💾 Guarda los cambios con un mensaje que describe el commit.
- **`git pull`**: 🔄 Trae cambios desde un repositorio remoto y los integra con tu rama actual.
- **`git push`**: 🚀 Sube tus cambios a un repositorio remoto.
- **`git branch`**: 🌿 Lista todas las ramas locales.
- **`git checkout <rama>`**: 🔀 Cambia a una rama específica.
- **`git checkout -b <nueva-rama>`**: 🌱 Crea una nueva rama y cambia a ella.
- **`git merge <rama>`**: 🤝 Fusiona la rama especificada con la rama actual.
- **`git log`**: 📜 Muestra el historial de commits.