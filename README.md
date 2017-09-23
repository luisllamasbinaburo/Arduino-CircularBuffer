# Librería Arduino Circular Buffer
La librería Circular Buffer implementa un Buffer Circular en Arduino. La clase Circular Buffer emplea templates para permitir funcionar con distintos tipos (int, long, float, …).

Más información https://www.luisllamas.es/libreria-arduino-circular-buffer/

## Instrucciones de uso
### Constructor
El Buffer Circular se instancia a través de su constructor que recibe el tamaño del Buffer como único parámetro.
```c++
CircularBuffer<int> circularBuffer(capacity);
```

### Obtener elementos
```c++
// Obtiene el elemento N
circularBuffer[N];

//Obtiene el primer elemento
circularBuffer.First();

//Obtiene los N primeros elementos
circularBuffer.First(numItems);

//Obtiene el último elemento
circularBuffer.Last();

//Obtiene los N últimos elementos
circularBuffer.Last(numItems);
```

### Añadir elementos
```c++
// Añade un elemento al final del buffer
circularBuffer.Add(T item);

// Inserta un elemento al principio del buffer
circularBuffer.Insert(T item);
```

### Eliminar elementos
```c++
// Elimina el primer elemento del buffer
circularBuffer.RemoveFirst();

// Elimina el último elemento del buffer
circularBuffer.RemoveLast();
```

### Extraer elementos
Obtienen y eliminan un elemento, útil para implementar colas y pilas de forma sencilla.
```c++
// Elimina el primer elemento, y devuelve el valor anterior
circularBuffer.ExtractFirst();

// Elimina el último elemento, y devuelve el valor anterior
circularBuffer.ExtractLast();
```

### Sustituir elementos
```c++
// Sustituye el primer elemento
circularBuffer.ReplaceFirst(item);

// Sustituye el último elemento
circularBuffer.ReplaceLast(item);

// Sustituye el elemento en el índice indicado
circularBuffer.ReplaceAt(index, item);
```

### Conversión
```c++
// Devuelve el buffer como un Array
circularBuffer.ToArray();

// Copia el contenido del buffer a un Array
circularBuffer.CopyTo(items);

// Rellena el buffer a partir del contenido de un Array
circularBuffer.FromArray(items, numItems);
```

## Ejemplos
La librería Circular Buffer incluye los siguientes ejemplos para ilustrar su uso.
* CircularBuffer: Ejemplo de uso para variables integer.
