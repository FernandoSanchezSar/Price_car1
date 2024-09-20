# Price_car
Practical Application Assignment 11.1: What Drives the Price of a Car?
## Resumen ejecutivo
El objetivo de la presente aplicación es comprender qué factores hacen que un auto sea más o menos costoso o dicho de otro modo, que es lo que valoran los clientes de una auto usado. Para lo grar este objetivo se usará tecnicas de selección de caracterísiticas y de regularización para evitar el overfiting.

## Técnicas usadas en la aplicación
Las técnicas que se han usado son: Sequential Feature Selection con estimator LinearRegresion(), Sequential Feature Selection con estimator Lasso(), Regularización Ridge, Regularización Lasso y Permutation Importance para cada uno de los modelos antes indicados.<br>
En este [link](https://github.com/FernandoSanchezSar/Kraftwerk/blob/main/prompt.ipynb) se encuentra el Jupiter notebook donde se han desarrollado los modelos.

## Resumen de los hallazgos
Consideramos que el modelo Regularización de Lasso se encuentra mas alineado a los datos de vehículos usados.<br>
1. Según nuestro análisis la característica del año al cuadrado y modelo del vehículo (year^2 model_target) es lo más valorado por el cliente a la hora de adquirir un vehículo usado.<br>
2. Como segunda caraterítica de importancia se encuentra la región, modelo y el estatus limpio del vehículo usado (region_target, model_target y title_status_clean).<br>
3. Como tercera característica de iportancia se encuentra el año del vehículo (year^3).<br>
4. Cuarta características mas valorada se encuentra el año, el modelo y el color del vehículo (year model_target paint_color_target).<br>
5. La quinta característica valorada se encuentra 6 cilindros, transmisión manual y tracción fwd ( cylinders_6 cylinders transmission_manual drive_fwd).<br>

## Siguientes pasos

Se decide no terminar el proyecto y pasar a una segunda iteración para mejorar los resultados. Se propondrá al negocio mayor tiempo para completar los sigueintes datos

1. Datos faltantes de la característica fabricante (manufacturer), que puede identificarse conociendo el modelo (model) y tanbién en sentido contrario completar el modelo conociendo el frabricante.
2. Validar la característica de condición para excluirlo considerando que un 41% tiene datos faltantes. Los datos faltantes se completaron con la moda del grupo de manufacturer y model, lo cuál no fue una buena idea.
3. La característica cylinders puede ser completada con ayuda del cliente, porque en la gran mayoria de los casos se puede determinar sabiendo la marca y el modelo (nanufacturer y model).
