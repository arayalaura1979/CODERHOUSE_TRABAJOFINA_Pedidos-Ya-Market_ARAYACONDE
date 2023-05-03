# CODERHOUSE_TRABAJOFINALII_ARAYACONDE
Trabajo final curso 32760-data-science

Integrantes: 
* Keren Conde 
* Maria Laura Araya

Objetivo: 
La empresa “Pedidos Ya Market” realiza ventas de productos por catálogo y web. El objetivo de este análisis se basa en encontrar tendencias y patrones de cuanto será el gasto futuro de los clientes tomando en consideración el perfil de cada tipo de clientes y las compras realizadas (por la web, por catálogos, con descuentos, etc) en la empresa “Pedidos Ya Market”.

Descripción del data Set 
La adquisición de datos corresponden a 5 campañas de encuestas promocionales
Descripción: 
* Year_Birth Año de Nacimiento 
* Education	Educación
* Marital_Status Estado Civil	 
* Income Ingresos 	
* Kidhome	número de niños pequeños en casa del cliente.
* Teenhome número de adolescentes en casa del cliente	
* Dt_Customer	fecha en la que el cliente se registró al CRM de la compañía.
* Recency	número de días que pasaron desde la última compra.
* MntWines cantidad gastada en vinos en los últimos dos años.	
* MntFruits  cantidad gastada en frutas en los últimos dos años.
* MntMeatProducts cantidad gastada en carne en los últimos dos años. 
* MntFishProducts cantidad gastada en pescado en los últimos dos años.
* MntSweetProducts cantidad gastada en dulces en los últimos dos años.
* MntGoldProds cantidad gastada en productos de oro en los últimos dos años.
* NumDealsPurchases número de compras realizadas con descuentos.
* NumWebPurchases número de compras realizadas en el sitio web.
* NumCatalogPurchases  numero de compras realizadas usando el catálogo.
* NumStorePurchases número de compras realizadas diractamente en tiendas
* NumWebVisitsMonth número de visitas realizadas al sitio web.
* AcceptedCmp3 1 si el cliente participó en la campaña 3 promocional.
* AcceptedCmp4 1 si el cliente participó en la campaña 4 promocional.
* AcceptedCmp5 1 si el cliente participó en la campaña 5 promocional. 
* AcceptedCmp1 1 si el cliente participó en la campaña 1 promocional. 
* AcceptedCmp2 1 si el cliente participó en la campaña 2 promocional.
* Complain 1 si el cliente ha presentado alguna queja en los últimos dos años.
* Z_CostContact Costo Contacto
* Z_Revenue Ingresos
* Response 

# Primero ver:  1 Carga y Transformaciones_ ArayaConde.ipynb
En esta etapa se realizaran las transfomraciones del data set necesarias para realizar el EDA y busqueda de Insights.
Transforamciones: 
* Trabajamos los null
* Nueva columna de monto total.
* Calculamos la edad
* Categorizamos la edad en Adulto mayor, adulto y joven.
* Eliminamos columnas con contantes
* Trabajamos los Outliers
* Nueva columna calculada con hijos totales

# Segundo ver: 2 Análisis_ ArayaCondeLerzo.ipynb
El área de marketing cuenta con científicos de datos que le permitirán analizar las compras que se realizaron en el pasado con el objetivo de entender comportamientos futuros. De esta manera las campañas de Marketing apuntaran a clientes específicos donde se conoce y espera un buen resultado. Propósitos: Establecer un modelo que permite la predicción de las ventas, mejorando con ello costos y creación de mejores estrategias. Determinar las técnicas de machine Learning para analizar las características de clientes que más compran y de esta manera lanzar campañas que apunten a los mismos.
En esta etapa planteamos las hipótesis para analizar las cuales son:

* ¿Los ingresos de los clientes tiene que ver con la cantidad de quejas en los 2 ultimos años?
* ¿Existe una relación entre el gasto realizado y el estudio de los consumidores?
* La cantidad de hijos menores o adolescentes esta relacionado con los gastos, de que tipo (pescado, vino, etc)
* ¿Existe una relación entre la cantidad gastada y el Estado civil?
* ¿Existe una relación entre la cantidad de compras en la web y el total de gastos?
* ¿Existe una relación entre el monto gastado total y los ingresos?
* ¿Como se relacionan las variables en general, que correlación tienen?
* ¿Que relación tiene los tipos de compras con las otras variables? Como por ejemplo con los descuentos o el numero de hijos

# Tercero ver: StoryTelling_ ArayaConde.ipynb
Data storytelling es un enfoque estructurado para comunicar información sobre los datos, utilizando elementos narrativos y elementos visuales. En este trabajo desarrollamos algunas hipotesis, las presentamos y las comprobamos.
Continuamos describriendo...
StoryTelling:
EDAD vs GASTOS: ¿La edad de los consumidores influye en la cantidad de compras y en la cantidad de Gastos?
* ¿Existe una relación entre la cantidad de compras de carne segun tenga hijos pequeños o adolecentes?
* ¿Existe una relación entre el importe gastado en golosinas y la cantidad de hijos sean niños y adolecentes?


# Cuarto ver: PCAyMODELOS__ArayaConde.ipynb
En este paso hacemos reducción de variables aplicando el algoritmo PCA, de 31 pasamos a tener 12 columnas. 
Luego realizamos tres modelos con diferentes con técnicas de aprendizaje supervisado: 
•	LinearRegression()
•	DecisionTreeRegressor()
•	RandomForestRegressor()
Realizamos evaluación de los modelos estadísticos y de aprendizaje, determinando la precisión y la calidad de las predicciones. Mediante:
•	MAE (Mean Absolute Error)
•	MSE (Mean Squared Error)
•	R² (Coeficiente de determinación)
•	MAPE (Mean Absolute Percentage Error)
En conclusión el modelo de Regresión lineal y Randon Forest obtiene mejores valores en la evaluación. 
Descartamos de nuestro análisis a el árbol de decisión por que hace overfitting (e ajusta demasiado bien a los datos de entrenamiento y, como resultado, no generaliza bien para nuevos datos de prueba).

# Quinta ver: 5_Cross_validation_LinearRegression__ArayaConde.ipynb y 5_Cross_validation_RandomForest__ArayaConde.ipynb
En la validación Cruzada aplicamos los métodos:
•	Cross-validation (validación cruzada) 
•	LeaveOneOut (dejar uno fuera)
•	K-Fold
En los tres obtenemos mejores resultados en el modelo de Random Forest. En conclusión, este es el que decidimos aplicar a nuestro trabajo Final. 
