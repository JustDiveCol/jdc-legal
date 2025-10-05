# 📘 JustDiveCol – Documentos Legales

Repositorio oficial que contiene los **documentos legales, formularios, políticas y descargos de responsabilidad** de **JustDiveCol S.A.S.**  
Este sitio se publica de manera automática mediante **GitHub Pages** y está disponible en:

👉 [https://legal.justdivecol.com](https://legal.justdivecol.com)

---

## 🗂️ Estructura del repositorio

```
jdc-legal/
├── .github/
│   └── workflows/
│       └── pages.yml           # Flujo de despliegue automático a GitHub Pages
├── docs/                       # Carpeta con todos los documentos PDF
│   ├── ACUERDO-DE-DESCARGO-DE-RESPONSABILIDAD-Y-ASUNCION-DE-RIESGO-VIAJES-Y-EXCURSIONES-JUSTDIVECOL.pdf
│   ├── ACUERDO-VOLUNTARIO-DE-DESCARGO-DE-RESPONSABILIDAD-Y-RENUNCIA-DE-DERECHOS-VIAJES-EN-BARCO-Y-BUCEO-JUSTDIVECOL.pdf
│   ├── CONTRATO-DE-DESCARGO-DE-RESPONSABILIDAD-Y-ASUNCION-DE-RIESGO-BUCEADORES-CERTIFICADOS-JUSTDIVECOL.pdf
│   ├── CONTRATO-DE-DESCARGO-DE-RESPONSABILIDAD-Y-ASUNCION-DE-RIESGO-GENERAL-JUSTDIVECOL.pdf
│   ├── DECLARACION-DE-COMPRENSION-DE-PRACTICAS-ESTANDARES-DE-BUCEO-SEGURO-JUSTDIVECOL.pdf
│   ├── INFORME-MEDICO-DEL-BUCEADOR-JUSTDIVECOL.pdf
│   └── POLITICAS-DE-SERVICIO-PROTECCION-DE-DATOS-Y-CODIGO-DE-CONDUCTA-JUSTDIVECOL.pdf
├── index.html                  # Página principal con enlaces a los documentos
├── CNAME                       # Dominio personalizado: legal.justdivecol.com
├── .gitignore
└── README.md
```

---

## ⚙️ Despliegue automático (GitHub Actions)

El archivo `.github/workflows/pages.yml` ejecuta el flujo de publicación mediante **GitHub Pages** cada vez que se actualiza la rama `main`.

### 🔁 Flujo resumido

1. GitHub Actions detecta un cambio en `main`.
2. Se ejecuta el flujo `pages.yml`.
3. Se empaquetan los archivos estáticos (`index.html`, `/docs`).
4. GitHub publica automáticamente en **https://legal.justdivecol.com**.

### 🧩 Configuración del dominio

- El archivo `CNAME` en la raíz del repo contiene:
  ```
  legal.justdivecol.com
  ```
- En los DNS del dominio, se debe tener un registro **CNAME** apuntando a:
  ```
  legal.justdivecol.com → <tuusuario>.github.io
  ```
- Una vez propagado, activa **Enforce HTTPS** en  
  _Settings → Pages → Enforce HTTPS._

---

## 🧪 Pruebas locales

Antes de subir cambios, puedes probar el sitio con:

### Opción 1 — Usando la extensión **Live Server** de VS Code

1. Instálala desde el marketplace.
2. Haz clic derecho sobre `index.html` → **“Open with Live Server”**.
3. Verás el sitio en `http://127.0.0.1:5500`.

### Opción 2 — Usando Node.js

```bash
npx serve .
```

Luego abre [http://localhost:3000](http://localhost:3000).

---

## 🧱 Cómo actualizar documentos

1. Sustituye o agrega nuevos PDF dentro de la carpeta `docs/`.  
   Se recomienda mantener el formato:
   ```
   NOMBRE-DE-DOCUMENTO-JUSTDIVECOL.pdf
   ```
2. Actualiza los títulos y enlaces en `index.html`.
3. Confirma y haz push a `main`:
   ```bash
   git add .
   git commit -m "Actualización de documentos legales"
   git push
   ```
4. GitHub Pages publicará los cambios automáticamente en unos segundos.

---

## 🛡️ Licencia y uso

Los documentos aquí contenidos son propiedad de **JustDiveCol S.A.S.**  
Su reproducción o uso fuera del contexto de las actividades de la empresa está prohibida sin autorización expresa.

© JustDiveCol S.A.S. – Todos los derechos reservados.
