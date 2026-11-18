# Publica tu primera página en AWS desde Nerdearla México

En este workshop vas a crear tu cuenta de AWS y publicar una página con una URL que puedes compartir. Vas a usar [AWS Amplify Hosting](https://aws.amazon.com/amplify/hosting/?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el), que toma el código de tu repositorio de GitHub y lo publica en AWS cada vez que haces un cambio.

## Lo que necesitas

- Una cuenta de GitHub
- Un navegador

No necesitas instalar nada en tu computadora.

## 1. Crea tu cuenta de AWS

Abre [este enlace para crear tu cuenta de AWS](https://signin.aws.amazon.com/signup?request_type=builderId&trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el) y completa el registro. Si eres elegible para AWS Free Tier, tu cuenta empieza en el **Free plan**, con USD 100 en créditos. El Free plan no genera cargos mientras no cambies al Paid plan.

## 2. Haz un fork del repositorio del workshop

1. Abre [este enlace para hacer un fork del repositorio del workshop](https://github.com/anacunha/nerdearla-mx-aws/fork).
2. Deja el nombre como está (o cámbialo si quieres) y haz clic en **Create fork**.

El repositorio es una página en `index.html` con sus estilos y el logo. No tiene `package.json` ni archivos de configuración.

## 3. Publica tu página con Amplify

1. Abre la [consola de Amplify](https://console.aws.amazon.com/amplify/create/repo-branch?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el).
2. Elige **GitHub** y haz clic en **Next**.
3. En la ventana de GitHub, autoriza a Amplify. Cuando te pregunte a qué repositorios puede acceder, elige **Only select repositories** y selecciona tu fork.
4. Selecciona tu repositorio y la rama `main`.
5. En **App settings**, mira la configuración de build. Amplify revisó tu repositorio, vio que no hay framework y va a publicar los archivos tal como están. No cambies nada.
6. Haz clic en **Next** hasta llegar a **Save and deploy**.

Amplify descarga tu código, lo publica y te muestra el progreso. Tarda alrededor de un minuto.

## 4. Abre tu URL

Cuando termine, haz clic en **Visit deployed URL**. Tu URL se ve así: `https://main.d1234abcd.amplifyapp.com`.

¡Esa página ya está en internet! Ábrela en tu celular para comprobarlo.

## 5. Cambia tu página

Ahora vas a ver lo que pasa cuando cambias el código.

1. En GitHub, abre `index.html` en tu repositorio y haz clic en el lápiz para editar.
2. Busca `Tu nombre` y cámbialo por tu nombre.
3. Haz clic en **Commit changes**.
4. Regresa a la consola de Amplify. Vas a ver un deploy nuevo que empezó solo.
5. Cuando termine, recarga tu URL.

No hiciste deploy a mano. Cada commit en `main` publica una versión nueva de tu página.

## Qué acaba de pasar

- **Hosting:** Amplify guarda tu página y la sirve desde la red de distribución de AWS (Amazon CloudFront), con HTTPS incluido.
- **Deploy continuo:** Amplify está conectado a tu repositorio. Cada commit en la rama conectada dispara un deploy nuevo.
- **Historial:** en la consola puedes ver cada deploy y qué commit lo generó.

## Comparte tu página

Deja tu URL en el [formulario del sorteo](https://pulse.amazon/survey/DT14IXHU) para participar por los premios.

## Qué sigue con Amplify

### Personaliza tu página con tu agente de código

Clona tu repositorio, abre la carpeta en tu agente de código (Kiro, Claude Code, Cursor, Codex o el que uses) y pídele cambios. Por ejemplo:

> Esta es una página estática publicada con AWS Amplify Hosting. Agrega una sección con mis redes sociales y las tres charlas que más me gustaron de Nerdearla México. No agregues un paso de build.

Cuando termine, revisa los cambios, haz commit y push a `main`. Amplify publica la versión nueva.

Si conectas el [Agent Toolkit for AWS](https://docs.aws.amazon.com/agent-toolkit/latest/userguide/what-is-agent-toolkit.html?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el), tu agente consulta la documentación actual de AWS y usa la skill de Amplify en lugar de adivinar.

### Agrega un backend con Amplify Gen 2

Tu página es solo frontend. Con [Amplify Gen 2](https://docs.amplify.aws/react/?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el) puedes agregar inicio de sesión, una base de datos y almacenamiento de archivos escribiendo TypeScript, y Amplify los despliega junto con tu frontend en cada commit. Empieza con el [quickstart de Amplify Gen 2](https://docs.amplify.aws/react/start/quickstart/?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el), que publica una app de tareas con base de datos y login.

### Usa tu propio dominio

Si tienes un dominio, puedes conectarlo a tu app de Amplify y Amplify crea el certificado HTTPS por ti. Revisa [cómo configurar un dominio propio](https://docs.aws.amazon.com/amplify/latest/userguide/custom-domains.html?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el).

## Si ya no la necesitas

En la consola de Amplify, abre tu app, ve a **App settings** → **General settings** y haz clic en **Delete app**. Eso borra la página publicada. Tu repositorio de GitHub sigue ahí.

## Recursos

- [AWS Amplify Hosting](https://docs.aws.amazon.com/amplify/latest/userguide/welcome.html?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el)
- [Documentación de Amplify Gen 2](https://docs.amplify.aws/react/?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el)
- [AWS Free Tier](https://aws.amazon.com/free/?trk=54e40584-a59e-4b8d-a5b4-ecfbd722ff7e&sc_channel=el)
