# Fundamentos de Bases de Datos — Pipeline SQLite

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/HaroldSthid/Fundamentals-BaseDatos-SQLite/blob/master/Fundamentos_BaseDatos_SQLite.ipynb)

Pipeline end-to-end de fundamentos de bases de datos, usando **SQLite** como motor, inspirado en la ruta de [VibePixel Academy — Baby Steps Tech](https://haroldsthid.github.io/VibePixel-AcademyBabyStepsTech/index.html#ruta).

## Qué hace el notebook

Dominio: **e-commerce** (clientes, categorías, productos, órdenes, líneas de orden, pagos).

1. **Diseño del Modelo ERM** — entidades, atributos, relaciones y cardinalidades, más el DDL de SQLite.
2. **Poblamiento de tablas** — datos sintéticos con [`Faker`](https://faker.readthedocs.io/), incluyendo problemas de calidad inyectados a propósito (duplicados, nulos, formatos inconsistentes).
3. **Data cleaning** — normalización con `pandas`: deduplicación, manejo de nulos, parsing de tipos, integridad referencial.
4. **Carga en SQLite** — persistencia del modelo limpio en `ecommerce.db`.
5. **Reporting** — tres queries SQL con visualización en `matplotlib`: ingresos por categoría/mes, top clientes por gasto, ticket promedio por país.

## Cómo correrlo

### Opción A — Google Colab (recomendado)
Click en el badge de arriba. Todas las celdas instalan sus propias dependencias (`Faker`); no necesitás configurar nada más.

### Opción B — Local
```bash
pip install -r requirements.txt
jupyter notebook Fundamentos_BaseDatos_SQLite.ipynb
```

## Estructura del repo

```
.
├── Fundamentos_BaseDatos_SQLite.ipynb   # notebook con el pipeline completo
├── requirements.txt                     # dependencias para correr local
└── .gitignore                           # ignora ecommerce.db y checkpoints
```

`ecommerce.db` se genera al ejecutar el notebook y no se versiona.
