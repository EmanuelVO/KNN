# KNN

1. Considere la base de datos “recursos_humanos.csv” sobre empleados que abandonan una empresa.

2. El objetivo es analizar porqué los empleados deciden irse con la competencia y éste podría ser un desafío serio para un departamento de recursos humanos, el cual se podría abordar mediante modelos predictivos de Machine Learning. Las variables manejadas son: 

satisfaction_level: Nivel de satisfacción. 

last_evaluation: Puntaje obtenido en la ultima evaluación.

average_montly_hours: Promedio de horas trabajadas al mes.

time_spend_company: Tiempo del usuario en la compañía. 

work_accident: Si el empleado ha tenido algún accidente laboral (1 = Sí, 0 = No).

promotion_last_5years: Si el empleado ha sido promovido en los últimos 5 años.

sales: Departamento donde trabaja. 

salary: Categoría del salario. 

left: Variable a predecir y si el empleado dejó o no la empresa (1 = Sí, 0 = No).

3. Cargue la base de datos en Python y asegúrese de re-codificar las variables categóricas de manera pertinente antes de iniciar su análisis (Sugerencia: Use “pd.get_dummies”)

Se recodificaron las variables 'sales' y 'salary'.

4. Mediante un análisis exploratorio de datos determine si esta base de datos está equilibrada o no (de acuerdo a las categorías existentes).

<img width="850" height="676" alt="image" src="https://github.com/user-attachments/assets/95480707-0bf6-4a32-8697-2d9ae5cdc47e" />

Corroboramos que todas las columnas contienen la misma cantidad de datos, por lo que esta base de datos está equilibrada. Ademas realizamos un histograma para observar la distribución de distintas variables. 

5. Use el método de K Vecinos más cercanos para generar un modelo predictivo. Para dicho fin, determine el valor óptimo de K evaluando distintas alternativas: k = 1, 2, ...., 20 Asegúrese de respaldar su recomendación de la k óptima en base a una tabla que compare en cada caso las diversas precisiones.

<img width="127" height="623" alt="image" src="https://github.com/user-attachments/assets/2456caca-4ffc-42c2-9f52-42bdc4848c80" />

k óptima: 1

6. Elabore un mapa de calor para la matriz de confusión asociada al valor óptimo de k. Interprete verbalmente cada resultado mostrado en dicha matriz.

<img width="453" height="443" alt="image" src="https://github.com/user-attachments/assets/739b00af-eaa4-46c7-8ffa-ad57d9023fce" />

Obtuvimos 3309 casos correctamente pronosticados en donde el empleado no se fue la compañía y 1011 casos correctamente pronosticados en donde el empleado dejó la compañía. Por otra parte, hubo 61 casos incorrectamente pronosticados en donde el empleado dejó la compañía y 119 casos incorrectamente pronosticados en donde el empleado no se fue la compañía. Este modelo es más preciso pronosticando los casos en los que el empleado no se va de la compañía. 

7. Obtenga e interprete la gráfica de la curva ROC para el valor óptimo de k.

<img width="574" height="450" alt="image" src="https://github.com/user-attachments/assets/ccd8cabf-a359-46f2-9948-cbb27dbab5da" />

El área debajo de la curva es de 0.95, bastante cercano a 1, por lo que se puede considerar que el modelo tiene buena presición. 
