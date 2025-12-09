portfolio-template/
├── index.html
├── 404.html
├── README.md
├── LICENSE
├── .gitignore
├── docs/ # Documentación y planes
│ └── plan.md # Plan de desarrollo con agentes de IA (si se usan)
├── assets/
│ ├── css/
│ │ ├── index.css # archivo “barrel”: centraliza todos los imports de CSS
│ │ ├── base.css # reset, variables, estilos de raíz
│ │ ├── layout.css # utilidades de layout/grid/flex
│ │ ├── components.css # estilos compartidos de componentes (botones, cards, etc.)
│ │ └── [otros].css # añade según necesidad
│ ├── js/
│ │ └── main.js
│ ├── images/ # idealmente CDN; si son locales, optimizadas y ligeras
│ └── fonts/ # si usas tipografías personalizadas (se prefieren las de sistema)
└── [configuración de build si aplica]
