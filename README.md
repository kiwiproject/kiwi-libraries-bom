# Kiwi Libraries Bill of Materials (BOM)

_TODO Add badges_

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
            <version>[current-version]</version> <!-- Replace with the latest version -->
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
