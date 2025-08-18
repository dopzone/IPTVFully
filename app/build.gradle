plugins {
    id 'com.android.application'
    id 'org.jetbrains.kotlin.android'
    id 'kotlin-kapt'                          // ✅ Required for Hilt
    id 'com.google.gms.google-services'       // ✅ Firebase
    id 'com.google.dagger.hilt.android'       // ✅ Hilt
}

android {
    namespace "com.fullyiptv"
    compileSdk 34

    defaultConfig {
        applicationId "com.fullyiptv"
        minSdk 21
        targetSdk 34
        versionCode 1
        versionName "1.0"
    }

    buildFeatures {
        compose true
    }

    composeOptions {
        kotlinCompilerExtensionVersion "1.5.1"   // ✅ match Kotlin 1.9.x
    }

    kotlinOptions {
        jvmTarget = "17"
    }
}

dependencies {
    // 🔥 Firebase
    implementation platform('com.google.firebase:firebase-bom:33.2.0')
    implementation 'com.google.firebase:firebase-analytics'

    // ✅ Core AndroidX
    implementation 'androidx.core:core-ktx:1.12.0'
    implementation 'androidx.appcompat:appcompat:1.7.0'

    // ✅ Jetpack Compose (required!)
    implementation "androidx.activity:activity-compose:1.8.2"
    implementation "androidx.compose.ui:ui:1.5.1"
    implementation "androidx.compose.ui:ui-tooling-preview:1.5.1"
    implementation "androidx.compose.material3:material3:1.1.2"
    debugImplementation "androidx.compose.ui:ui-tooling:1.5.1"
    debugImplementation "androidx.compose.ui:ui-test-manifest:1.5.1"
    androidTestImplementation "androidx.compose.ui:ui-test-junit4:1.5.1"

    // ✅ Hilt
    implementation "com.google.dagger:hilt-android:2.48"
    kapt "com.google.dagger:hilt-compiler:2.48"

    // ✅ Pin error_prone_annotations
    implementation "com.google.errorprone:error_prone_annotations:2.11.0"
}

// 🚫 Disable error-prone checks
tasks.withType(JavaCompile).configureEach {
    options.compilerArgs += ["-Xlint:none", "-proc:none"]
}
