# Desplegué esto en AWS desde Nerdearla México

Repositorio del workshop de AWS en Nerdearla México. Es una página estática que publicas con [AWS Amplify Hosting](https://aws.amazon.com/amplify/hosting/) conectando este repositorio desde la consola. No necesitas instalar nada.

## Cómo usarla

1. Haz clic en **Fork** → **Create fork**.
2. Abre la [consola de Amplify](https://console.aws.amazon.com/amplify/create/repo-branch), elige **GitHub** y selecciona tu fork y la rama `main`.
3. Haz clic en **Save and deploy**.
4. Cuando termine, abre **Visit deployed URL**.

Para cambiar tu página, edita `index.html` y haz commit en `main`. Amplify la vuelve a publicar automáticamente.

## Qué hay aquí

```
├── index.html          ← tu página
├── styles.css
├── nerdearla-logo.webp
└── favicon.png
```

No hay `package.json` ni archivo de configuración: Amplify detecta que es un sitio estático y publica los archivos tal como están.
