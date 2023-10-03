```
# Manipulación de datos
import pandas as pd

# Manipulación de arreglos y matrices
import numpy as np

data = pd.read_excel('AlturasPesos.xlsx')

data.head()

X = data[['Altura']].copy()
y = data[['Peso']].copy()

X.head()

y.head()

# Importa LinearRegression
from sklearn.linear_model import LinearRegression # Reemplaza por LinearRegression

# Inicializa el modelo con el nombre de una variable -- tu elijes cómo llamarlo
Model = LinearRegression() # Reemplaza con el nombre de tu modelo

# Entrenas el modelo con los datos - permites que se "ajuste" a tus inputs y variables objetivo
# El modelo aprende de los datos disponibles, y determina cómo se comportan
Model.fit('Altura', 'Peso') # Reemplaza con el nombre de tu modelo. Luego, dentro del paréntesis, debes colo

pronostico_pesos = Model.predict(X) # Reemplaza con el nombre de tu modelo.

comparacion = pd.DataFrame({
    'Pesos Pronosticados': pd.DataFrame(pronostico_pesos)[0],
    'Pesos Verdaderos': y['Peso'].values
})

comparacion

Importa mean_squared_error
from sklearn.metrics import ____ # Reemplaza por mean_squared_error

# Calcula el rmse, metiendo los (1) valores reales y (2) el pronóstico a la función
rmse = mean_squared_error(y, pronostico_pesos, squared=False) # Reemplaza con la variable que contiene tu pronóstico

print(f"El RMSE de tu modelo de regresión lineal es de: {rmse}.")



