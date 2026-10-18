# Simulador de Pipeline y Dependencias | Arquitectura de Computadores

Repositorio oficial para el desarrollo del **Proyecto 3 de Arquitectura de Computadores I (GR20)** en el Tecnológico de Costa Rica (TEC). Consiste en un simulador modular desarrollado en **C11** para evaluar el desempeño de un **pipeline de 5 etapas** y cómo el uso de rutas de **forwarding** puede reducir el impacto de las **dependencias**.

---

## 👥 Integrantes

| Nombre Completo | Carné | Usuario de GitHub |
| :--- | :---: | :---: |
| **Luis Pablo Vargas Muñoz** | `2021490483` | [@SkyVM888](https://github.com/SkyVM888) |
| **Carlos Daniel Hurtado Villalobos** | `2021067615` | [@Charlespixel](https://github.com/Charlespixel) |
| **Brayan Ariel Vargas Rojas** | `2021028522` | [@BrayanVR21](https://github.com/BrayanVR21) |

---

## 🛠️ Estructura del Proyecto (FALTA EDITAR)

* **`main.c`**: xxx.
* **`cache.c` / `cache.h`**: xxx.
* **`leer.c`**: xxx.
* **`Pruebas/`**: xxx (`.txt`).

---

## 📐 Especificaciones de la Arquitectura Simulada (FALTA EDITAR)

* **Espacio de Direccionamiento:** 16 bits sin signo (64 KiB).
* **Capacidad Total de Caché:** 64 Bytes.
* **Tamaño de Bloque:** 16 Bytes.
* **Organizaciones Evaluadas:**
  * **Caché Directa:** 4 conjuntos, 1 vía por conjunto ($10\text{ bits Tag}, 2\text{ bits Index}, 4\text{ bits Offset}$).
  * **Caché 2 Vías:** 2 conjuntos, 2 vías por conjunto ($11\text{ bits Tag}, 1\text{ bit Index}, 4\text{ bits Offset}$).
* **Política de Reemplazo:** LRU (*Least Recently Used*) para la organización de 2 vías.
* **Métrica de Rendimiento (AMAT):** 
  $$\text{AMAT} = 1 + \left(\frac{\text{Fallos}}{\text{Accesos Totales}}\right) \times 20\text{ ciclos}$$

---

## ⚙️ Compilación y Ejecución (FALTA EDITAR/VERIFICAR)

### Prerrequisitos
* Compilador **GCC 15.2.0** (Built by MSYS2 project) o superior con soporte para **C11**.

Para verificar la versión en tu sistema:
```bash
gcc --version
```
### Compilación

Compila todos los módulos fuente utilizando las banderas de advertencia estándar:

```bash
gcc -std=c11 -Wall -Wextra -o main.exe main.c    
```

### Ejecución

Para ejecutar el simulador pasando como parámetro la ruta de un archivo de prueba ubicado en la carpeta `pruebas/`:

```bash
./main.exe pruebas/{nombre_del_archivo}.txt
```
**Ejemplo de ejecución:**

```bash
./main.exe pruebas/conflicto.txt
```

## 📄 Archivos de Entrada (Pruebas/*.txt) (FALTA EDITAR)

Los archivos de prueba deben incluir direcciones numéricas en formato decimal (ej. 0, 32) separadas por saltos de línea.

```bash
0
32
64
0
0
96
```

## 📊 Formato de Salida (FALTA EDITAR)


El programa despliega en consola:

1. Traza Paso a Paso: Muestra para cada acceso la dirección enviada, sus campos extraídos (Tag, Index, Offset), el resultado del acceso (HIT / MISS) y la vía afectada o reemplazada.

2. Resumen de Métricas: Tabla comparativa final entre la caché directa y la de 2 vías con total de accesos, aciertos, fallos, Hit Rate, Miss Rate y valor de AMAT.

## 🚀 Entrega Oficial - Proyecto 2: Simulador de Memoria Caché en C11

Esta etiqueta ([`p2-entrega`](https://github.com/SkyVM888/ADC1-P2-GrupoPCB/releases/tag/p2-entrega)) marca la versión final y funcional del simulador de memoria caché de 16 bits desarrollado en C11, correspondiente al curso de Arquitectura de Computadores (GR20).
