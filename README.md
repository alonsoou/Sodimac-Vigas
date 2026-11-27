# Constructor de vigas

App web de una sola página para armar el plano de vigas de un rack arrastrando las piezas, y exportarlo como imagen a Excel.

## Cómo usar

Abre `index.html` en Chrome o Edge (doble clic). No necesita instalación ni internet: la librería de Excel está en `vendor/`.

- **Agregar**: arrastra una pieza al rack, o tócala para ponerla en el primer espacio libre. Secciones: **Vigas** (Inicio 10, Viga 7, Viga 10, Término 10), **Vigas traseras** (término 10, dibujada al 70% de opacidad) y **Aditamentos** (panel con gancheras, charola —con rejilla, lisa o con divisores—, canastilla colgante, canasto con ruedas, carrito con ruedas, viga + tarima, frente —siempre dentro del rack y detrás de los aditamentos— y fondo: paneles de 30 cm apilados entre pilares de góndola, de color a elegir, detrás de todo; bandeja metálica 2 posiciones y barra de carga con gancheras, que van en la columna izquierda, derecha o en ambas).
- **Mover**: arrastra una pieza desde cualquier parte. Las asas para estirar aparecen solo en la pieza seleccionada, y la pieza seleccionada se puede arrastrar aunque esté detrás de otra. En *Piezas en el rack* puedes seleccionar cualquier pieza de la lista.
- **Modelos de ejemplo**: "Viga Default" (rack 61/365/122 solo con viga de inicio y término) y "Góndola con fondos" (rack 56/365/250 con fondos de 30 cm, pilares, barras de carga y bandejas).
- **Modo noche / modo luz**: botón en el encabezado. La imagen para Excel siempre sale con fondo blanco.
- **Logo**: el encabezado muestra `logo.svg`; reemplaza ese archivo para cambiarlo.
- **Mover**: arrastra la viga. Se ajusta a las perforaciones (los números azules de 1 a 48). El número amarillo indica la perforación donde está la viga.
- **Panel, charola, carrito, casetón**: arrástralos para moverlos; arrastra su borde superior o inferior para cambiar el alto. En "Selección" se cambian barras de ganchos, canastos por nivel, separador, cantidad de carritos, número de paneles y color del casetón.
- **Eliminar**: arrastra la pieza fuera del rack, o selecciónala y pulsa `Supr`.
- `↑` / `↓` mueven la pieza seleccionada 1 perforación (`Shift` = 5). `Ctrl+Z` deshace.
- El dibujo se guarda solo en el navegador.

## Exportar a Excel

- **Descargar Excel nuevo**: crea un `.xlsx` con la imagen en el rango indicado (por defecto `D8:H50`) y el resumen de vigas debajo.
- **Usar mi plantilla**: carga tu `.xlsx`, elige la hoja y pulsa *Insertar en plantilla*. La imagen se dibuja con la proporción exacta de las celdas `D8:H50` de esa hoja, así que no queda estirada. Si ya había una imagen en ese rango, se reemplaza.
- **PNG / Copiar imagen**: para pegarla a mano en Excel.

> Nota: la plantilla se reescribe con ExcelJS. Las celdas, formatos, colores e imágenes se conservan, pero los gráficos y las formas dibujadas (no imágenes) pueden perderse. Revisa el archivo la primera vez.
