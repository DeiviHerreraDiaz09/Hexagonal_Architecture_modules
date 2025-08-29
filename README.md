# Hexagonal Architecture Modules ✅

Este repositorio contiene un proyecto desarrollado con Spring Boot que implementa la arquitectura hexagonal (Ports and Adapters) organizada por contextos. El objetivo principal es lograr una estructura de código limpia, desacoplada y fácilmente escalable, donde cada contexto representa un dominio o subdominio independiente dentro de la aplicación.

## Características principales

- **Spring Boot:** Framework que facilita la creación de aplicaciones Java empresariales, proporcionando configuración automática y una amplia integración con el ecosistema Spring.
- **Arquitectura Hexagonal:** Permite separar la lógica de negocio (dominio) de los detalles de infraestructura (persistencia, servicios externos, etc.) mediante el uso de puertos y adaptadores.
- **Contextos:** El código está organizado por contextos, cada uno con su propio dominio, aplicación e infraestructura, lo que facilita la mantenibilidad y la evolución independiente de cada módulo.

## Estructura del proyecto

```
src/
	main/
		java/
			com/
				example/
					demo/
						context/
							_user/
								application/
								domain/
								infraestructura/
							_product/
							shared/
		resources/
			application.properties
```

- Cada contexto (por ejemplo, `_user`, `_product`) contiene sus propias capas de dominio, aplicación e infraestructura.
- La carpeta `shared` incluye componentes reutilizables entre contextos.

## ¿Por qué arquitectura hexagonal?

La arquitectura hexagonal ayuda a:

- Mantener el núcleo de negocio independiente de frameworks y tecnologías externas.
- Facilitar la realización de pruebas unitarias y de integración.
- Permitir la integración sencilla de nuevos adaptadores (por ejemplo, diferentes bases de datos, APIs externas).

## Ejecución

Para ejecutar el proyecto:

```bash
./mvnw spring-boot:run
```

## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o un pull request para sugerencias o mejoras.
