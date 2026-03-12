# Fur-Hair

> Sistema de shaders para cabello y pelo en **Unity 6 (URP)**, pensado para crear resultados visuales estilizados y/o realistas en tiempo real.

![Banner del proyecto Fur-Hair](https://github.com/user-attachments/assets/844f0b7f-0c85-4f01-9426-a49e22f9cc4e)

## 📌 Descripción

**Fur-Hair** es un proyecto orientado a la experimentación y desarrollo de materiales/shaders para representar pelo y cabello dentro de Unity. La base actual está configurada sobre **Universal Render Pipeline (URP)** y preparada para evolucionar hacia un paquete reutilizable.

## ✨ Características actuales

- Proyecto configurado en **Unity 6**.
- Pipeline gráfico con **URP**.
- Estructura organizada por áreas: programación, arte, escenas, presets y settings.
- Escenas de trabajo para iterar shaders y look-dev.
- Flujo de publicación automatizable mediante **GitHub Actions** (release → npm).

## 🧱 Stack técnico

- **Unity**: `6000.3.10f1`
- **Render Pipeline**: `com.unity.render-pipelines.universal@17.3.0`
- **Visual Effects**: `com.unity.visualeffectgraph@17.3.0`
- **XR/OpenXR**: `com.unity.xr.meta-openxr@2.4.0`

## 📂 Estructura del repositorio

```text
Assets/
├─ 1-Programming/
├─ 2-Art/
├─ 3-Scenes/
├─ 4-Presets/
├─ 5-Settings/
└─ XR/

ProjectSettings/
Packages/
.github/workflows/
```

## 🚀 Primeros pasos

### 1) Clonar el repositorio

```bash
git clone https://github.com/<tu-usuario>/Fur-Hair.git
cd Fur-Hair
```

### 2) Abrir en Unity Hub

1. Abre **Unity Hub**.
2. Selecciona **Add project** y elige esta carpeta.
3. Usa la versión **6000.3.10f1** (o compatible).

### 3) Ejecutar escenas de prueba

- Revisa `Assets/3-Scenes/` para abrir las escenas disponibles.
- Ajusta materiales/luces para validar comportamiento del shader en distintos escenarios.

## 🧪 Flujo recomendado de desarrollo

1. Crea una rama por feature (`feature/nombre-cambio`).
2. Trabaja los shaders/materiales en escena de pruebas.
3. Valida rendimiento visual (distancia, iluminación, sombras, aliasing).
4. Documenta parámetros y resultados antes de merge.

## 📦 Publicación (CI/CD)

El repositorio incluye un workflow en GitHub Actions que se ejecuta al crear un **release** y:

- Calcula la versión desde el tag (`vX.Y.Z`).
- Sincroniza el `README.md` al paquete.
- Publica en npm usando `NPM_TOKEN_PACKAGE`.

> Nota: el directorio objetivo del paquete se deriva del nombre del repositorio (`Packages/com.jaimecamacho.<repo>`).

## 🗺️ Roadmap sugerido

- [ ] Shader base para hebras con anisotropía.
- [ ] Parámetros de peinado (dirección, densidad, variación).
- [ ] LODs/material variants para rendimiento.
- [ ] Escena benchmark para medir FPS y calidad.
- [ ] Documentación visual de presets (capturas + valores).

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para colaborar:

1. Haz fork del proyecto.
2. Crea tu rama (`feature/mi-aporte`).
3. Envía un Pull Request con contexto técnico, capturas y validaciones.

## 📄 Licencia

Este proyecto se distribuye bajo la licencia indicada en [`LICENSE`](./LICENSE).
