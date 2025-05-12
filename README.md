# orion-aar

📦 Orion AAR — Android Performance Monitoring SDK

Orion is a lightweight performance monitoring library for Android apps. It captures critical runtime metrics including:
	•	⏱️ App startup (TTID & TTFD)
	•	🧠 Janky and frozen frames
	•	🌐 Network requests per activity
	•	📉 Crash and ANR reporting (customizable)

 🛠 Integration Steps

 1. Add GitHub Packages Repository

In your settings.gradle.kts:
```kotlin
dependencyResolutionManagement {
    repositories {
        google()
        mavenCentral()
        maven {
            url = uri("https://maven.pkg.github.com/epsilondelta-speed/orion-aar")
            credentials {
                username = project.findProperty("gpr.user") as String? ?: System.getenv("GPR_USER")
                password = project.findProperty("gpr.key") as String? ?: System.getenv("GPR_KEY")
            }
        }
    }
}
```
Add these to your gradle.properties or environment:

```text
gpr.user=YOUR_GITHUB_USERNAME
gpr.key=YOUR_GITHUB_PERSONAL_ACCESS_TOKEN
```

2. Add the Dependency
   In build.gradle.kts of your app module:
   ```kotlin
   dependencies {
    implementation("co.epsilondelta:orion:1.0.0")
}
```

🧪 Sample Usage
```kotlin
EdOrion.initialize(application)
```
Track metrics, lifecycle, and network automatically once initialized.

🔐 Privacy Note

Only the AAR binary is published. The source code is private and not available in this repository.

📞 Need Help?

Visit Epsilon Delta or Contact Us(https://www.epsilondelta.co/contact) for integration assistance, enterprise licensing, or support.

📝 License

© 2025 Epsilon Delta. All rights reserved. Use of this plugin is subject to Epsilon Delta Orion’s terms.



