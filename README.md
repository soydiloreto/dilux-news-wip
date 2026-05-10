# dilux-news (WIP)

> ⚠️ **Repo intermedio privado.** Sandbox del template forkeable de Dilux News antes de publicar al repo final público.
>
> - **Repo final público (futuro)**: `soydiloreto/dilux-news` (con template flag activado)
> - **Estado actual**: Fase I del plan de migración (ver `dilux-news-core-wip/docs/plan.md`)

## Qué es esto

Repo template **mínimo** que los end-users clickean **"Use this template"**. El user obtiene una copia con su `config.yaml` + workflows que corren `pip install -U dilux-news` desde PyPI.

Cero código de engine vive acá — todo está en el package PyPI. Los workflows son shims minimales que delegan al CLI `dilux-news`.

## Estructura

```
dilux-news/
├── README.md                ← (esto, en versión final será el quick-start del user)
├── LICENSE                  ← Apache 2.0
├── config.example.yaml      ← config base, el user lo personaliza
├── briefs/.gitkeep          ← carpeta donde el cron auto-commitea briefs
├── .github/workflows/
│   ├── daily.yml            ← shim cron diario: pip install -U dilux-news && dilux-news run
│   └── setup.yml            ← shim wizard navegador: dilux-news setup-from-inputs ...
└── .gitignore
```

## Plan de migración

Ver `dilux-news-core-wip/docs/plan.md` para el plan ejecutable completo y estado.
