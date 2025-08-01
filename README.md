# Kiwi Libraries Bill of Materials (BOM)

[![build](https://github.com/kiwiproject/kiwi-libraries-bom/actions/workflows/build.yml/badge.svg)](https://github.com/kiwiproject/kiwi-libraries-bom/actions/workflows/build.yml)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=kiwiproject_kiwi-libraries-bom&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=kiwiproject_kiwi-libraries-bom)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Maven Central](https://img.shields.io/maven-central/v/org.kiwiproject/kiwi-libraries-bom)](https://central.sonatype.com/artifact/org.kiwiproject/kiwi-libraries-bom/ )

This is a Maven Bill of Materials (BOM) for use by projects that depend on one or more libraries
from the [kiwiproject](https://github.com/kiwiproject) organization.

It defines the latest versions of all officially published kiwiproject libraries, allowing you
to manage them centrally and use consistent versions across your projects.

To use this BOM in your Maven project, first import it in the `<dependencyManagement>` section:

```xml

<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>org.kiwiproject</groupId>
            <artifactId>kiwi-libraries-bom</artifactId>
            <version>[current-version]</version> <!-- Replace 'current-version' with the latest version -->
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

Then declare kiwiproject dependencies like this:

```xml

<dependencies>
    <dependency>
        <groupId>org.kiwiproject</groupId>
        <artifactId>kiwi</artifactId>
    </dependency>

    <dependency>
        <groupId>org.kiwiproject</groupId>
        <artifactId>retrying-again</artifactId>
    </dependency>

    <dependency>
        <groupId>org.kiwiproject</groupId>
        <artifactId>kiwi-test</artifactId>
        <scope>test</scope>
    </dependency>
</dependencies>
```

📌 Tip: See the [Releases](https://github.com/kiwiproject/kiwi-libraries-bom/releases) page for the latest version.
