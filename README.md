# microbean-abstract-environment

The `microbean-abstract-environment` consists primarily of a mildly
opinionated `pom.xml` file that describes runtime dependencies that
together make up part of a bare minimum microBean environment.

A full microBean environment&mdash;even a minimal one&mdash;will also
need a CDI 2.0 implementation.

The `pom.xml` file also produces a Docker image that collects those
dependencies together in a root `/microbean` directory, together with
an Alpine Linux variant of the Java development kit.

Users of this project are either Java developers&mdash;who can include
the `pom.xml` directly as a dependency&mdash;or developers of Docker
images for microBean projects (a CDI 2.0 implementation and its
dependencies is needed to complete any environment).

## Components

The `microbean-abstract-environment` environment consists of versions
of the following:

* [Version 3.0.1-b09 of the reference implementation][uel-ri] of [JSR
  341][jsr-341], the Java Expression Language specification.
* [Version 6.0.7.Final of the Hibernate Validator CDI
  extension][hibernate-validator-cdi].  This requires an
  implementation of [JSR 341][jsr-341], which is enumerated above.
* [Version 0.3.0 of microBean Configuration][microbean-configuration].
* [Version 0.3.0 of microBean Configuration
  CDI][microbean-configuration-cdi].
* [Version 6 of microBean Main][microbean-main].
  
Together these implement [version 0.1.0 of the microBean Base
Specification][microbean-base-specification].
  
[uel-ri]: https://javaee.github.io/uel-ri/
[jsr-341]: https://jcp.org/en/jsr/detail?id=341
[hibernate-validator-cdi]: https://docs.jboss.org/hibernate/validator/6.0/reference/en-US/html_single/#section-getting-started-cdi
[microbean-configuration]: https://microbean.github.io/microbean-configuration/
[microbean-configuration-cdi]: https://microbean.github.io/microbean-configuration-cdi/
[microbean-main]: https://ljnelson.github.io/microbean-main/
[microbean-base-specification]: https://microbean.github.io/microbean-base-specification/
