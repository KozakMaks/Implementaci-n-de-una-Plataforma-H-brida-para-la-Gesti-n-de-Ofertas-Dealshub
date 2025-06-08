# Dealshub

*TFG 2024/2025*

**Plataforma híbrida (web y móvil) para la detección y gestión de chollos con recomendación inteligente**

---

## Índice

- [Descripción](#descripción)
- [Autores](#autores)
- [Demo en producción](#demo-en-producción)
- [Repositorio](#repositorio)
- [Tecnologías](#tecnologías)
- [Instalación y uso](#instalación-y-uso)
- [Licencia](#licencia)

---

## Descripción

Dealshub es el proyecto de fin de grado en Desarrollo de Aplicaciones Multiplataforma (TFG 2024/2025). Ofrece una solución completa para buscar, filtrar y recomendar ofertas (*chollos*) de productos. Integra un sistema de recomendación basado en IA y cumple con estándares de accesibilidad (WCAG 2.1) y calidad de software (ISO/IEC 25010).

## Autores

- **Maksim Romanyuk**
- **Yevgenyy Yefremenko**

## Demo en producción

- Web: [https://dealhub-tfg.vercel.app/](https://dealhub-tfg.vercel.app/)
- ![image](https://github.com/user-attachments/assets/600e6516-5599-4fa2-8a9d-386f567740e6)


## Repositorio

El código fuente de la aplicación web y el APK móvil se encuentran en este repositorio:

```
https://github.com/KozakMaks/Implementaci-n-de-una-Plataforma-H-brida-para-la-Gesti-n-de-Ofertas-Dealshub
```

## Tecnologías

- **Frontend:** Next.js 14, Tailwind CSS, shadcn/ui
- **Backend:** Firebase (Cloud Functions, Firestore, Hosting)
- **IA/PLN:** OpenAI GPT-3.5 / Llama-7B fine-tuned
- **Recomendación:** Filtrado colaborativo, Annoy (Approx-NN)
- **CI/CD:** GitHub Actions, Cypress, Jest, SonarCloud
- **Notificaciones:** Firebase Cloud Messaging

## Instalación y uso

1. **Clonar repositorio**

   ```bash
   git clone https://github.com/KozakMaks/Implementaci-n-de-una-Plataforma-H-brida-para-la-Gesti-n-de-Ofertas-Dealshub.git
   cd Implementaci-n-de-una-Plataforma-H-brida-para-la-Gesti-n-de-Ofertas-Dealshub
   ```

2. **Instalar dependencias**

   ```bash
   pnpm install
   ```

3. **Configurar variables de entorno**

   Crea un archivo `.env.local` con las credenciales:

   ```text
   NEXT_PUBLIC_FIREBASE_API_KEY=...
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=...
   FIREBASE_PRIVATE_KEY=...
   OPENAI_API_KEY=...
   ```

4. **Ejecutar en modo desarrollo**

   ```bash
   pnpm dev
   ```

   Accede a la app en `http://localhost:3000`.

5. **Construir y desplegar**

   ```bash
   pnpm build
   pnpm start
   ```

6. **Generar APK móvil**

   La generación del APK se realiza mediante TWA. El paquete resultante está en la carpeta `apk/` tras ejecutar:

   ```bash
   pnpm build:apk
   ```

## Licencia

Este proyecto está bajo la licencia MIT.

