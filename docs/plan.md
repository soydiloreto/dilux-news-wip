# Plan de migración

El plan ejecutable completo (6 fases, checkpoints, estado actual) vive en:

**`/Users/pablodiloreto/news-repos/dilux-news-core-wip/docs/plan.md`**

Este repo (`dilux-news-wip`) es solo el **template**. El plan general se mantiene en el repo del engine para no duplicar.

## Lo que toca a este repo en cada fase

- **Fase 0** ✅: scaffold del template (este archivo, README, LICENSE Apache 2.0, config.example.yaml, workflows shim).
- **Fase I**: refinar workflows shim conforme se define el CLI en `dilux-news-core-wip`. Ajustar `setup.yml` con todos los inputs del wizard navegador.
- **Fase II**: cambiar `daily.yml` para apuntar a TestPyPI temporalmente (`pip install -i https://test.pypi.org/simple/ -U dilux-news`). Validar end-to-end con cuenta secundaria.
- **Fase III**: revertir `daily.yml` a PyPI real. Crear `soydiloreto/dilux-news` público con commit limpio copiando el contenido final de este wip.
- **Fase IV+**: este repo (wip) ya cumplió su función — borrar al final.

## Restricción dura

Cero modificaciones a `soydiloreto/dilux-news-alpha`.
