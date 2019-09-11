# microBean™ Abstract Environment

The microBean™ Abstract Environment project consists primarily of a
mildly opinionated `pom.xml` file that describes runtime dependencies
that together make up part of a bare minimum microBean™ environment.

A full microBean™ environment&mdash;even a minimal one&mdash;will also
need a CDI 2.0 implementation.

The `pom.xml` file also produces a Docker image that collects those
dependencies together in a root `/microbean` directory, together with
an Alpine Linux variant of the OpenJDK Java development kit.

Users of this project are either Java developers&mdash;who can include
the `pom.xml` directly as a dependency&mdash;or developers of Docker
images for microBean™ projects (a CDI 2.0 implementation and its
dependencies is needed to complete any environment).

## Components

The `microbean-abstract-environment` environment consists of versions
of the following:

* [Version 3.0.3 of the Reference Implementation of the Jakarta
  Expression Language](https://eclipse-ee4j.github.io/el-ri/)
* [Version 6.0.17.Final of the Hibernate Validator CDI
  extension](https://docs.jboss.org/hibernate/validator/6.0/reference/en-US/html_single/#section-getting-started-cdi)
* [Version 0.5.0 of microBean™
  Configuration](https://microbean.github.io/microbean-configuration/)
* [Version 0.5.0 of microBean™ Configuration
  CDI](https://microbean.github.io/microbean-configuration-cdi/)
* [Version 8 of microBean™
  Main](https://ljnelson.github.io/microbean-main/)

Together these implement parts of [version 0.5.0 of the microBean™
Base
Specification](https://microbean.github.io/microbean-base-specification/).
