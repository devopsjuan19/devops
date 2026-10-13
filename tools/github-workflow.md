# Flujo de trabajo básico con GitHub

## Paso 1: Crear un repositorio en GitHub

1. **Inicia sesión** en tu cuenta de GitHub.
2. Haz clic en el **botón +** (esquina superior derecha) → **New repository**.
3. Completa los campos:
   - **Repository name**: elige un nombre para tu proyecto
   - **Description** (opcional): descripción del proyecto
   - **Public** o **Private**: según el tipo de proyecto
4. **Desmarca** todas las casillas de inicialización:
   - ❌ Initialize this repository with a README
   - ❌ Add .gitignore
   - ❌ Add a license
5. Haz clic en **Create repository**.

## Paso 2: Clonar el repositorio a tu máquina local

```bash
# Copia la URL HTTPS o SSH del repositorio desde GitHub
# Ejemplo con HTTPS:
git clone https://github.com/tu-usuario/nombre-del-repositorio.git

# O usando SSH:
git clone git@github.com:tu-usuario/nombre-del-repositorio.git

# Navega al directorio del proyecto
cd nombre-del-repositorio
```

## Paso 3: Trabajar con cambios

### Verificar el estado de los archivos
```bash
git status
```

### Editar archivos
Modifica tus archivos con tu editor favorito...

### Preparar cambios (staging)
```bash
# Agregar todos los archivos modificados y nuevos
git add .

# Agregar un archivo específico
git add nombre-del-archivo.txt

# Agregar múltiples archivos específicos
git add archivo1.txt archivo2.py
```

### Guardar cambios localmente
```bash
git commit -m "Descripción clara y concisa de los cambios"

# Ejemplos:
git commit -m "Add user authentication feature"
git commit -m "Fix login validation error"
git commit -m "Update README with setup instructions"
```

## Paso 4: Subir cambios a GitHub

### Primer push (conecta el origen si es necesario)
```bash
git push -u origin main
# o si tu rama principal se llama 'master':
git push -u origin master
```

### Push posterior (después del primer push)
```bash
git push
```

## Flujo completo de ejemplo

```bash
# 1. Clonar (solo la primera vez)
git clone https://github.com/tu-usuario/mi-proyecto.git
cd mi-proyecto

# 2. Crear una rama para nuevos cambios (recomendado)
git checkout -b feature/nueva-funcionalidad

# 3. Trabajar en los archivos...
# editar archivos

# 4. Ver estado
git status

# 5. Agregar cambios al staging
git add .

# 6. Commit
git commit -m "Implementar nueva funcionalidad"

# 7. Subir a GitHub
git push -u origin feature/nueva-funcionalidad

# 8. Crear Pull Request en GitHub (desde la web)
```

## Comandos útiles adicionales

```bash
# Ver historial de commits
git log --oneline

# Ver cambios no staged
git diff

# Volver a estado anterior del último commit (sin borrar cambios)
git reset --soft HEAD~1

# Descargar cambios de GitHub sin fusionar
git fetch

# Actualizar tu rama local con cambios de GitHub
git pull
```