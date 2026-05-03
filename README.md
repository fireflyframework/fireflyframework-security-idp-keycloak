# Firefly Framework - IDP - Keycloak

[![CI](https://github.com/fireflyframework/fireflyframework-idp-keycloak/actions/workflows/ci.yml/badge.svg)](https://github.com/fireflyframework/fireflyframework-idp-keycloak/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Java](https://img.shields.io/badge/Java-21%2B-orange.svg)](https://openjdk.org)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-green.svg)](https://spring.io/projects/spring-boot)

> Keycloak implementation of the Firefly IDP adapter with admin API integration and REST controller.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

## Overview

Firefly Framework IDP Keycloak implements the `IdpAdapter` interface using Keycloak as the identity provider. It provides user management, authentication, token operations, and administrative functions through both the Keycloak Admin REST API and the token endpoint.

The module includes `IdpAdapterImpl` as the main adapter, backed by `IdpUserService` for user-facing operations, `IdpAdminService` for administrative functions, and `TokenService` for token management. It features a built-in `IdpController` REST endpoint for direct IDP operations and a `KeycloakExceptionHandler` for standardized error responses.

Auto-configuration is provided via `KeycloakAutoConfiguration` with configurable connection properties through `KeycloakProperties`.

## Features

- Full `IdpAdapter` implementation using Keycloak Admin API
- Built-in `IdpController` REST endpoint for IDP operations
- User service for authentication, registration, and profile management
- Admin service for realm and user administration
- Token service for token exchange, refresh, and introspection
- `KeycloakClientFactory` and `KeycloakAPIFactory` for API connection management
- CORS configuration for cross-origin requests
- Keycloak-specific exception handler
- Spring Boot auto-configuration via `KeycloakAutoConfiguration`
- Configurable via `KeycloakProperties`

## Requirements

- Java 21+
- Spring Boot 3.x
- Maven 3.9+
- Keycloak server instance

## Installation

```xml
<dependency>
    <groupId>org.fireflyframework</groupId>
    <artifactId>fireflyframework-idp-keycloak</artifactId>
    <version>26.02.07</version>
</dependency>
```

## Quick Start

```xml
<dependencies>
    <dependency>
        <groupId>org.fireflyframework</groupId>
        <artifactId>fireflyframework-idp</artifactId>
    </dependency>
    <dependency>
        <groupId>org.fireflyframework</groupId>
        <artifactId>fireflyframework-idp-keycloak</artifactId>
    </dependency>
</dependencies>
```

## Configuration

```yaml
firefly:
  idp:
    keycloak:
      server-url: http://localhost:8080
      realm: my-realm
      client-id: my-app
      client-secret: my-secret
```

## Documentation

No additional documentation available for this project.

## Contributing

Contributions are welcome. Please read the [CONTRIBUTING.md](CONTRIBUTING.md) guide for details on our code of conduct, development process, and how to submit pull requests.

## License

Copyright 2024-2026 Firefly Software Foundation.

Licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE) for details.
