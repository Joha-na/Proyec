# Procesador de Transacciones en Paralelo

## Información Institucional

- **Institución:** Escuela Politécnica Nacional
- **Carrera:** Ciencia de Datos e Inteligencia Artificial
- **Integrantes:**
  - Ámbar Salazar
  - Erick Páez
  - Adrián Trujillo
  - Mauro Valencia
  - Brenda Veintimilla

---

## 1. Descripcion del Problema

El programa limpia, imputa y normaliza un archivo CSV con transacciones de ventas, comparando el rendimiento entre:

- **Modo Secuencial**: Procesamiento con un solo hilo
- **Modo Paralelo**: Procesamiento con 3 hilos simultaneos

### Dataset
- 5000 transacciones de ventas
- Columnas: ID, Monto, Cantidad, Categoria, Region, Descuento
- Datos con valores nulos (celdas vacias)

---

## 2. Estructuras de Datos

### Transaccion

```c
typedef struct {
    int    id;
    double monto;
    int    cantidad;
    char   categoria[64];
    char   region[64];
    double descuento;
    
    int monto_nulo;
    int cantidad_nulo;
    int descuento_nulo;
    int categoria_nula;
    int region_nula;
    
    double monto_norm;
    double cantidad_norm;
    double descuento_norm;
} Transaccion;
