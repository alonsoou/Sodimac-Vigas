# Editor de Vigas (rack)

App web de una sola página para armar el plano de vigas de un rack arrastrando las piezas, y exportarlo como imagen a Excel.

## Cómo usar

Abre `index.html` en Chrome o Edge (doble clic). No necesita instalación ni internet: la librería de Excel está en `vendor/`.

- **Agregar**: arrastra una pieza (Inicio 10, Viga 7, Viga 10, Término 10, Panel) al rack, o tócala para ponerla en el primer espacio libre.
- **Mover**: arrastra la viga. Se ajusta a las perforaciones (los números azules de 1 a 48). El número amarillo indica la perforación donde está la viga.
- **Panel**: arrástralo para moverlo; arrastra su borde superior o inferior para cambiar el alto. En "Selección" se cambia la cantidad de barras de ganchos.
- **Eliminar**: arrastra la pieza fuera del rack, o selecciónala y pulsa `Supr`.
- `↑` / `↓` mueven la pieza seleccionada 1 perforación (`Shift` = 5). `Ctrl+Z` deshace.
- El dibujo se guarda solo en el navegador.

## Exportar a Excel

- **Descargar Excel nuevo**: crea un `.xlsx` con la imagen en el rango indicado (por defecto `D8:H50`) y el resumen de vigas debajo.
- **Usar mi plantilla**: carga tu `.xlsx`, elige la hoja y pulsa *Insertar en plantilla*. La imagen se dibuja con la proporción exacta de las celdas `D8:H50` de esa hoja, así que no queda estirada. Si ya había una imagen en ese rango, se reemplaza.
- **PNG / Copiar imagen**: para pegarla a mano en Excel.

> Nota: la plantilla se reescribe con ExcelJS. Las celdas, formatos, colores e imágenes se conservan, pero los gráficos y las formas dibujadas (no imágenes) pueden perderse. Revisa el archivo la primera vez.
