// Root-level build.gradle

buildscript {
    repositories {
        google()
        mavenCentral()
    }
    dependencies {
        // ✅ Core Gradle Plugins
        classpath "com.android.tools.build:gradle:8.4.2"
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:1.9.0"

        // ✅ Firebase Google Services plugin (must stay here)
        classpath "com.google.gms:google-services:4.4.2"

        // ❌ Hilt plugin removed (now handled via plugins{} DSL in /app/build.gradle)
    }
}

allprojects {
    repositories {
        google()
        mavenCentral()
    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}
