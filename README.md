# microbean-abstract-environment

The `microbean-abstract-environment` consists primarily of a `pom.xml`
file that describes runtime dependencies that together make up the
bare minimum microBean environment.

The `pom.xml` file also produces a Docker image that collects those
dependencies together in a root `/microbean` directory, together with
an Alpine Linux variant of the Java development kit.

Users of this project are either Java developers&mdash;who can include
the `pom.xml` directly as a dependency&mdash;or developers of Docker
images for microBean projects (a CDI 2.0 implementation and its
dependencies is needed to complete any environment).
