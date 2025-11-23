# 📊 Clash Royale Big Data Analytics con MongoDB

Este proyecto implementa una base de datos NoSQL orientada a documentos utilizando **MongoDB** para gestionar y analizar estadísticas del videojuego "Clash Royale". El objetivo es migrar datos estructurados (CSV) a un formato flexible (BSON) para ejecutar operaciones CRUD y pipelines de agregación avanzada.

**Curso:** Big Data - UNAD  
**Tarea:** 4 - Almacenamiento y Consultas de Datos  
**Autores:** Jhon Alejandro Patiño López & Eduardo Daza Canizares

## 🚀 Objetivos del Proyecto
1. Migrar datos de archivos planos (`.csv`) a una colección en MongoDB.
2. Implementar operaciones CRUD para la gestión del inventario de cartas.
3. Generar *insights* sobre el balance del juego mediante `Aggregation Framework`.

## ⚙️ Configuración del Entorno

### Requisitos
* MongoDB Community Server o MongoDB Atlas.
* MongoDB Compass (Interfaz Gráfica).
* MongoDB Shell (`mongosh`).

### 1. Importación de Datos
El dataset original se encuentra en la carpeta `/data`. 
* **Base de Datos:** `TAREA4-BIGDATA`
* **Colección:** `clash_royale_cards`
* **Tipo de Importación:** CSV con detección automática de tipos de datos.

---

## 💻 Consultas y Operaciones (Scripts)

Las consultas detalladas se encuentran en la carpeta `/src`. A continuación, un resumen de las operaciones principales realizadas.

### 1. Limpieza de Datos (DELETE)
Eliminación de cartas legendarias con datos corruptos (hitpoints nulos o NaN).

### 2. Inserción de Nuevas Cartas (INSERT)
Se agregaron cartas personalizadas al mazo:
* **Golem de Hielo** (Rare Troop)
* **Flechas** (Common Spell)

### 3. Actualización de Balance (UPDATE)
Modificación de estadísticas ("Buff") para la carta *Flechas*, aumentando su daño de 200 a 333.

### 4. Análisis de Datos (AGGREGATIONS)
Se implementaron pipelines para responder preguntas de negocio:
* Conteo de cartas agrupadas por rareza (`$group`).
* Filtros de cartas con puntos de vida bajos (`$match` + `$lt`).
* Proyección de cartas "tanque" (vida > 1500) mostrando solo nombre y tipo de ataque.

---
**Disclaimer:** Proyecto realizado con fines académicos para la Universidad Nacional Abierta y a Distancia (UNAD).
