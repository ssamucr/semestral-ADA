# 🏋️ Aplicación Web para Registro y Seguimiento de Rutinas de Entrenamiento

## 📘 Descripción del Proyecto

Este proyecto consiste en una aplicación web que permite a los usuarios registrar, gestionar y analizar rutinas de entrenamiento físico. A través de una interfaz intuitiva, el usuario puede crear rutinas personalizadas, registrar ejercicios, series, repeticiones y pesos utilizados. Además, la aplicación ofrece visualización del progreso mediante gráficas y estadísticas.

La solución está construida completamente sobre servicios de **AWS en la capa gratuita**, empleando una arquitectura **serverless** para garantizar escalabilidad, bajo costo y facilidad de mantenimiento.

## 🎯 Objetivos

- Permitir el registro estructurado de rutinas y entrenamientos.
- Brindar seguimiento al desempeño físico del usuario.
- Visualizar métricas clave mediante gráficas interactivas.
- Aplicar servicios de computación en la nube con arquitectura sin servidor.

## 🧱 Arquitectura General

```plaintext
Frontend (React) - alojado en Amazon S3 + CloudFront
↓
API Gateway (REST)
↓
Funciones AWS Lambda (Python)
↓
Amazon DynamoDB (persistencia de datos)
```


## 🧰 Tecnologías y Servicios Usados

| Componente       | Tecnología/Servicio    | Descripción                               |
|------------------|------------------------|-------------------------------------------|
| Frontend         | React + Chart.js       | Interfaz del usuario y gráficas           |
| Hosting Frontend | Amazon S3 + CloudFront | Sitio estático seguro y escalable         |
| Backend API      | AWS Lambda + API GW    | Lógica de negocio y endpoints REST        |
| Base de Datos    | Amazon DynamoDB        | Almacenamiento NoSQL de rutinas y sesiones |
| Autenticación    | Amazon Cognito (opcional) | Gestión de usuarios (signup/signin)   |
| CI/CD (opcional) | AWS SAM / GitHub Actions | Automatización del despliegue           |

## 📊 Funcionalidades Principales

- Registro de usuarios (si se usa Cognito)
- Crear y editar rutinas personalizadas
- Registro de sesiones de entrenamiento por día
- Ingreso de ejercicios, series, repeticiones y peso
- Visualización de estadísticas de progreso:
  - Peso total levantado
  - Volumen por músculo
  - Número total de repeticiones
- Sistema de temporizador de entrenamiento (opcional)

## 🚀 Despliegue

El proyecto fue desplegado completamente en la **capa gratuita de AWS**, usando:

- `AWS SAM` para la definición de infraestructura
- `Amazon S3` para el hosting del frontend
- `Amazon API Gateway` para la exposición de endpoints
- `AWS Lambda` para funciones serverless
- `Amazon DynamoDB` como base de datos
- `Amazon CloudWatch` para monitoreo y logs

## ⏳ Próximas Mejores / Extensiones Futuras

- Incorporación de inteligencia artificial para la generación automática de rutinas basadas en objetivos físicos.
- Módulo de recomendaciones de peso y descansos.
- Modo de entrenamiento en tiempo real con temporizador activo.
- Sistema de notificaciones por correo o push (SES/SNS).

## 📅 Cronograma de Trabajo

| Fecha           | Actividad                                                    |
|------------------|--------------------------------------------------------------|
| 5 de julio       | Definición y planificación del alcance                       |
| 6-9 de julio     | Desarrollo del backend: Lambda, API Gateway, DynamoDB        |
| 10-13 de julio   | Desarrollo del frontend + integración                        |
| 14-16 de julio   | Implementación de gráficas y seguimiento de entrenamientos   |
| 17-18 de julio   | Pruebas funcionales, documentación y presentación final      |

## 👤 Autor

Samuel Castro  
Facultad de Ingeniería en Desarrollo de Software  
Universidad Tecnológica de Panamá  
Julio 2025

