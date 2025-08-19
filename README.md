
> Diagrama representativo del flujo de ramas en Git Flow.  
- Fuente: Atlassian Docs ([enlace](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow))

![Git Flow Branches](https://nvie.com/img/git-model@2x.png)

![Estructura](https://i.ibb.co/Q3BBN2Vr/Captura-de-pantalla-2025-08-19-110939.png)

> Estructura de ramas según la metodología Git Flow.  
([enlace](https://nvie.com/posts/a-successful-git-branching-model/))

Este proyecto utiliza la metodología **Git Flow** para la gestión de ramas y versiones.

## Estructura de ramas

- **main**: Rama principal, contiene el código en producción.
- **develop**: Rama de desarrollo, integra nuevas funcionalidades antes de pasar a producción.
- **feature/**: Ramas para nuevas funcionalidades. Se crean desde `develop` y se fusionan en `develop`.
- **release/**: Ramas para preparar nuevas versiones. Se crean desde `develop` y se fusionan en `main` y `develop`.
- **hotfix/**: Ramas para corregir errores críticos en producción. Se crean desde `main` y se fusionan en `main` y `develop`.

## Flujo de trabajo

1. **Nueva funcionalidad**  
    Crear rama `feature/nombre` desde `develop`.  
    Al finalizar, fusionar en `develop`.

2. **Preparar una versión**  
    Crear rama `release/x.x.x` desde `develop`.  
    Realizar pruebas y ajustes.  
    Fusionar en `main` y `develop`.  
    Etiquetar la versión en `main`.

3. **Corrección urgente**  
    Crear rama `hotfix/x.x.x` desde `main`.  
    Solucionar el error.  
    Fusionar en `main` y `develop`.  
    Etiquetar la versión en `main`.

## Comandos útiles

```bash
git flow init
git flow feature start <nombre>
git flow feature finish <nombre>
git flow release start <versión>
git flow release finish <versión>
git flow hotfix start <versión>
git flow hotfix finish <versión>
```

## Recomendaciones

- Realizar commits descriptivos.
- Mantener ramas actualizadas.
- Eliminar ramas locales y remotas tras fusionar.

---
> Basado en la metodología [Git Flow](https://nvie.com/posts/a-successful-git-branching-model/)