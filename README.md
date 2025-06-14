# Domain Event Versioned Outbox Library

Biblioteca Java para implementar el patrón Outbox con eventos versionados de dominio, compatible con diferentes agregados y persistencia independiente.  
Ideal para arquitecturas orientadas a dominio que requieren garantizar la consistencia eventual entre la base de datos y los sistemas de mensajería (Kafka, RabbitMQ, etc.).

## Características

- Soporte para eventos versionados con esquema abierto.
- Gestión genérica de eventos y agregados.
- Persistencia y outbox desacoplados (compatible con JOOQ u otros).
- Dispatcher para publicación fiable de eventos.
- Transacciones atómicas entre persistencia y almacenamiento de eventos outbox.

## Uso

1. Define tus eventos versionados implementando `VersionedEvent`.
2. Extiende `AggregateRoot` para tus entidades de dominio.
3. Usa el repositorio genérico para persistir agregados.
4. Implementa un `DomainEventPublisher` para tu broker de eventos.
5. Configura y ejecuta el `OutboxEventDispatcher` para publicar eventos.

## Documentación

- [Especificación funcional](docs/FunctionalSpecification.md)
- [Ejemplos y guías](examples/)

## Contribuciones

Bienvenidas! Por favor sigue las guías en [CONTRIBUTING.md].

## Licencia

MIT License © Roberto

------------------------------------------------------------------------------------------

# Domain Event Versioned Outbox Library

Java library to implement the Outbox pattern with versioned domain events, compatible with different aggregates and persistence-agnostic.  
Ideal for domain-driven architectures that require eventual consistency between the database and messaging systems (Kafka, RabbitMQ, etc.).

## Features

- Support for versioned events with open schema.
- Generic management of events and aggregates.
- Decoupled persistence and outbox (compatible with JOOQ or others).
- Dispatcher for reliable event publishing.
- Atomic transactions between persistence and outbox event storage.

## Usage

1. Define your versioned events by implementing `VersionedEvent`.
2. Extend `AggregateRoot` for your domain entities.
3. Use the generic repository to persist aggregates.
4. Implement a `DomainEventPublisher` for your event broker.
5. Configure and run the `OutboxEventDispatcher` to publish events.

## Documentation

- [Functional specification](docs/FunctionalSpecification.md)
- [Examples and guides](examples/)

## Contributions

Welcome! Please follow the guidelines in [CONTRIBUTING.md].

## License

MIT License © Roberto