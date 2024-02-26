# Beta Bank ¿Un cliente dejará el banco pronto?

## Como contactarme
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andres946/)
[![Correo Electrónico](https://img.shields.io/badge/Correo%20Electrónico-andresgvelasquez8@gmail.com-red?style=for-the-badge&logo=mail.ru)](mailto:andresgvelasquez8@gmail.com)  

## Descripción del proyecto
Los clientes de Beta Bank se están yendo, cada mes, poco a poco. Los banqueros descubrieron que es más barato salvar a los clientes existentes que atraer nuevos.
Necesitamos predecir si un cliente dejará el banco pronto. Tú tienes los datos sobre el comportamiento pasado de los clientes y la terminación de contratos con el banco.
Crea un modelo con el máximo valor F1 posible. Para aprobar la revisión, necesitas un valor F1 de al menos 0.59. Verifica F1 para el conjunto de prueba. 
Además, debes medir la métrica AUC-ROC y compararla con el valor F1.

## Diccionario de datos

Ubicación: `../datasets/Churn.csv`  
  
1. Características:
    - RowNumber: índice de cadena de datos
    - CustomerId: identificador de cliente único
    - Surname: apellido
    - CreditScore: valor de crédito
    - Geography: país de residencia
    - Gender: sexo
    - Age: edad
    - Tenure: período durante el cual ha madurado el depósito a plazo fijo de un cliente (años)
    - Balance: saldo de la cuenta
    - NumOfProducts: número de productos bancarios utilizados por el cliente
    - HasCrCard: el cliente tiene una tarjeta de crédito (1 - sí; 0 - no)
    - IsActiveMember: actividad del cliente (1 - sí; 0 - no)
    - EstimatedSalary: salario estimado
2. Objetivo
    - Exited: El cliente se ha ido (1 - sí; 0 - no)

## Instalación de dependencias

Para instalar las dependencias necesarias para este proyecto, puedes ejecutar el siguiente comando:

```bash
pip install -r requirements.txt
```
**Nota** Esta versión de Boruta puede arrojar un error al utilizar np.float, np.int y np.bool. Basta con reemplazarlos por
float, int, bool respectivamente en el archivo donde este el error. 