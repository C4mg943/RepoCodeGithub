# 🚀 Guía Completa para Subir un Proyecto Nuevo a GitHub

Esta guía explica cómo subir un proyecto desde tu PC (VS Code) a un repositorio nuevo en GitHub y cómo trabajar después con él.

---

# 📌 PASO A PASO DESDE CERO

## 1️⃣ Crear repositorio en GitHub

1. Ir a GitHub.
2. Crear un repositorio nuevo.
3. IMPORTANTE:
   - ❌ NO marcar "Add README"
   - ❌ NO agregar `.gitignore`
   - ❌ NO agregar licencia

El repositorio debe estar completamente vacío.

---

## 2️⃣ Entrar a la carpeta del proyecto

```bash
cd ruta/de/tu/proyecto
```

Ejemplo:

```bash
cd C:\Users\USUARIO\Documentos\Proyecto
```

---

## 3️⃣ Inicializar Git

```bash
git init
```

---

## 4️⃣ Agregar todos los archivos

```bash
git add .
```

---

## 5️⃣ Crear el primer commit

```bash
git commit -m "Primer commit"
```

---

## 6️⃣ Conectar el proyecto con GitHub

```bash
git remote add origin https://github.com/USUARIO/NOMBRE-REPO.git
```

Reemplazar:
- `USUARIO` por tu usuario de GitHub
- `NOMBRE-REPO` por el nombre del repositorio

---

## 7️⃣ Asegurar que la rama sea main

```bash
git branch -M main
```

---

## 8️⃣ Subir el proyecto

```bash
git push -u origin main
```

Listo. El proyecto queda conectado al repositorio.

---

# 🔁 PARA FUTUROS CAMBIOS

Cada vez que hagas cambios en tu proyecto:

```bash
git add .
git commit -m "Descripción del cambio"
git push
```

---

# ⚠️ ERRORES COMUNES Y SOLUCIONES

## ❌ error: remote origin already exists

Significa que ya habías conectado un repositorio antes.

Solución:

```bash
git remote remove origin
git remote add origin URL_DEL_REPO
```

---

## ❌ error: src refspec main does not match any

Significa que no has hecho commit todavía.

Solución:

```bash
git add .
git commit -m "Primer commit"
git push -u origin main
```

---

# 🧠 FLUJO RÁPIDO RESUMIDO

Si quieres hacerlo rápido sin leer todo:

```bash
git init
git add .
git commit -m "Primer commit"
git remote add origin URL
git branch -M main
git push -u origin main
```

---

# 🔥 EXTRA (BUENA PRÁCTICA)

Si es proyecto web o con dependencias (Node, React, etc.), crea un `.gitignore` antes de hacer commit.

Ejemplo básico para Node:

```
node_modules/
.env
dist/
build/
```

Luego:

```bash
git add .
git commit -m "Configuración inicial"
git push
```

---

# ✅ Listo

Con esto puedes crear y subir cualquier proyecto nuevo sin volver a enredarte.
