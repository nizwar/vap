# VAP Android Player - JitPack Integration

[![](https://jitpack.io/v/nizwar/vap.svg)](https://jitpack.io/#nizwar/vap)

This library is available through JitPack. To use it in your Android project:

## Installation

### Step 1: Add JitPack repository to your root `build.gradle`:

```gradle
allprojects {
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```

### Step 2: Add the dependency to your app `build.gradle`:

```gradle
dependencies {
    implementation 'com.github.nizwar:vap:Tag'
}
```

Replace `Tag` with the latest release tag or commit hash.

## Usage

### Basic Usage

```kotlin
import com.tencent.qgame.animplayer.AnimView

// In your Activity or Fragment
val animView = findViewById<AnimView>(R.id.anim_view)

// Load and play animation
animView.setVideoFromAssets("your_animation.mp4")
animView.setListener(object : IAnimListener {
    override fun onVideoComplete() {
        // Animation completed
    }
    
    override fun onVideoDestroy() {
        // Animation destroyed
    }
    
    override fun onVideoRender(frameIndex: Int, config: AnimConfig?) {
        // Frame rendered
    }
    
    override fun onVideoStart() {
        // Animation started
    }
})

animView.startPlay()
```

### Advanced Usage

Check the [main documentation](../README.md) for advanced features like:
- Mask animations
- Mix mode
- Custom configurations
- Audio support

## Requirements

- Android API 16+
- Kotlin support

## License

See the [LICENSE](../LICENSE.txt) file for license rights and limitations.
