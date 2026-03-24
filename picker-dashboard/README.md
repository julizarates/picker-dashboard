# Picker Dashboard — Turbo

Dashboard de ranking de pickers por tienda con métricas de cancelaciones, stockouts, defectos y velocidad.

## Estructura
```
picker-dashboard/
├── index.html        ← Dashboard principal
├── data/
│   └── data.json     ← Datos de pickers (actualizar cada lunes)
└── README.md
```

## Cómo actualizar los datos cada lunes

1. Correr esta query en Snowflake
2. Exportar resultado como JSON
3. Guardar como `data/data.json` en este repo
4. GitHub Pages actualiza automáticamente en ~1 minuto

## Formato del JSON

```json
[
  {
    "picker": "Nombre Apellido",
    "tienda": "Turbo Chapinero",
    "pais": "CO",
    "cancelaciones": 0.8,
    "cancelaciones_lw": 1.1,
    "stockouts": 1.2,
    "stockouts_lw": 1.4,
    "defectos": 0.5,
    "defectos_lw": 0.7,
    "velocidad": 4.2,
    "velocidad_lw": 4.5
  }
]
```

## Activar GitHub Pages

1. Ir a Settings → Pages
2. Source: Deploy from a branch
3. Branch: main / (root)
4. Guardar → el link queda en `https://TU_USUARIO.github.io/picker-dashboard`
