# Sitio web de pareja

Proyecto de la Práctica de Laboratorio N° 2 — **Versionamiento de Aplicaciones**
Asignatura: Fundamentos de Sistemas Web · Universidad de las Fuerzas Armadas ESPE

## Objetivo

Desarrollar un sitio web sencillo, hecho únicamente con HTML, y gestionar sus versiones con Git y GitHub usando ramas de funcionalidad, desarrollo, pruebas y producción.

## Integrantes

| Estudiante | Rama de funcionalidad | Responsabilidad |
|---|---|---|
| Jeffry (Estudiante 1) | `feature-jeffry` | Página principal (`index.html`) y navegación entre páginas |
| Iker (Estudiante 2) | `feature-iker` | Página secundaria `pasatiempos.html` con listas, tabla y contenido multimedia |

## Funcionalidades implementadas

- Página principal con menú de navegación hacia todas las páginas.
- Página "Sobre nosotros" con información de la pareja.
- Página "Pasatiempos" con:
  - lista no ordenada, lista ordenada (`type="I"`) y lista anidada;
  - tabla con `caption`, encabezados `th`, `rowspan` y `colspan`;
  - imagen con atributos `src`, `alt`, `width` y `height`;
  - video con `controls`, `width` y `poster`;
  - enlaces internos (`#lista`, `#tabla`, `#multimedia`) y enlaces entre páginas.

## Estructura de archivos

```
sitio-web-parejas/
├── index.html
├── sobre-nostros.html
├── pasatiempos.html
├── imagenes/
│   └── pasatiempos.png
├── multimedia/
│   └── video.mp4
└── README.md
```

## Estructura de ramas

| Rama | Propósito |
|---|---|
| `main` | Producción: versión final aprobada |
| `pruebas` | Validación del sitio antes de pasar a producción |
| `desarrollo` | Integración de las funcionalidades |
| `feature-jeffry` | Funcionalidad del Estudiante 1 |
| `feature-iker` | Funcionalidad del Estudiante 2 |

Flujo: `feature-*` → `desarrollo` → `pruebas` → `main`.

## Comandos utilizados

```bash
git clone https://github.com/J3ffry1/sitio-web-parejas.git
git switch feature-iker
git status
git add .
git commit -m "Mensaje descriptivo"
git push
git switch desarrollo
git pull origin desarrollo
git merge feature-iker
git push origin desarrollo
git branch -a
git log --oneline --graph --all
git remote -v
```

## Cómo visualizar el sitio

1. Clonar el repositorio: `git clone https://github.com/J3ffry1/sitio-web-parejas.git`
2. Abrir la carpeta en Visual Studio Code.
3. Abrir `index.html` con doble clic (o clic derecho → *Abrir con* → navegador).
4. Navegar entre las páginas con el menú.

## Protección de la rama main

La rama `main` está protegida en GitHub (*Settings → Branches → Add branch protection rule*): no se permiten cambios directos y todo cambio debe entrar mediante un Pull Request con al menos una aprobación.
