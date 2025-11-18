---
name: mobile-games
description: Build mobile apps with React Native and Flutter, native iOS/Android development with Swift and Kotlin. Create games with modern game engines. Master cross-platform development for iOS, Android, and game platforms. Use when developing mobile applications, games, or cross-platform solutions.
---

# Mobile & Game Development Skill

## Quick Start

### React Native Application
```javascript
import React, { useState } from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

export default function App() {
    const [count, setCount] = useState(0);

    return (
        <View style={styles.container}>
            <Text style={styles.title}>Counter App</Text>
            <Text style={styles.count}>{count}</Text>
            <Button
                title="Increment"
                onPress={() => setCount(count + 1)}
            />
        </View>
    );
}

const styles = StyleSheet.create({
    container: { flex: 1, justifyContent: 'center', alignItems: 'center' },
    title: { fontSize: 24, marginBottom: 20 },
    count: { fontSize: 40, marginBottom: 20 },
});
```

### Flutter Widget
```dart
import 'package:flutter/material.dart';

void main() {
    runApp(const MyApp());
}

class MyApp extends StatefulWidget {
    const MyApp({Key? key}) : super(key: key);

    @override
    State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
    int _counter = 0;

    @override
    Widget build(BuildContext context) {
        return MaterialApp(
            home: Scaffold(
                appBar: AppBar(title: const Text('Counter')),
                body: Center(
                    child: Column(
                        mainAxisAlignment: MainAxisAlignment.center,
                        children: [
                            Text('$_counter', style: const TextStyle(fontSize: 40)),
                            ElevatedButton(
                                onPressed: () => setState(() => _counter++),
                                child: const Text('Increment'),
                            ),
                        ],
                    ),
                ),
            ),
        );
    }
}
```

### Swift & SwiftUI
```swift
import SwiftUI

struct ContentView: View {
    @State private var count = 0

    var body: some View {
        VStack(spacing: 20) {
            Text("Counter")
                .font(.largeTitle)
            Text("\(count)")
                .font(.system(size: 40))
            Button("Increment") {
                count += 1
            }
            .buttonStyle(.bordered)
        }
        .padding()
    }
}

#Preview {
    ContentView()
}
```

### Kotlin & Android
```kotlin
import android.os.Bundle
import androidx.appcompat.app.AppCompatActivity
import androidx.compose.foundation.layout.*
import androidx.compose.material3.*
import androidx.compose.runtime.*
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            CounterApp()
        }
    }
}

@Composable
fun CounterApp() {
    var count by remember { mutableStateOf(0) }

    Column(
        modifier = Modifier.fillMaxSize(),
        horizontalAlignment = Alignment.CenterHorizontally,
        verticalArrangement = Arrangement.Center
    ) {
        Text("Counter", fontSize = 24.sp)
        Text("$count", fontSize = 40.sp)
        Button(onClick = { count++ }) {
            Text("Increment")
        }
    }
}
```

## Mobile Development Patterns

### React Native
- **Navigation:** React Navigation, deep linking
- **State Management:** Redux, Context, Zustand
- **Networking:** Fetch API, axios, apollo-client
- **Local Storage:** AsyncStorage, SQLite, Realm
- **Performance:** FlatList, memoization, native modules
- **Testing:** Jest, React Native Testing Library

### Flutter
- **Navigation:** Navigator, GoRouter, auto_route
- **State Management:** Provider, Bloc, Riverpod, GetX
- **HTTP:** http package, dio, chopper
- **Local Storage:** shared_preferences, hive, sqflite
- **Performance:** Const constructors, lazy loading
- **Plugins:** pub.dev ecosystem

### Native iOS (Swift)
- **SwiftUI Framework:** Declarative UI, state binding
- **Navigation:** NavigationStack, NavigationLink
- **Networking:** URLSession, async/await
- **Local Storage:** Core Data, UserDefaults
- **Lifecycle:** App, Scene, View lifecycle
- **Testing:** XCTest, UI testing

### Native Android (Kotlin)
- **Jetpack Compose:** Modern declarative UI
- **Lifecycle:** Activity, Fragment, ViewModel
- **Networking:** Retrofit, OkHttp, coroutines
- **Room Database:** Type-safe database abstraction
- **Dependency Injection:** Hilt, Dagger
- **Testing:** JUnit, Espresso, Compose Testing

## Game Development Fundamentals

### Game Loop Architecture
```
while (game_running) {
    // Update game state
    update(delta_time)

    // Render graphics
    render()

    // Handle input
    handle_input()

    // Maintain frame rate
    sleep_until_next_frame()
}
```

### Game Development Concepts
- **Game Loop:** Update, render, input cycle
- **Physics:** Collision, gravity, movement
- **Rendering:** Sprites, meshes, shaders, cameras
- **Input:** Keyboard, mouse, touch, controller
- **Audio:** Sound effects, music, spatial audio
- **Optimization:** LOD, culling, batching

### Game Engines

#### Unity
- **Language:** C#, supports 25+ platforms
- **Editor:** Intuitive visual editor
- **Features:** Physics, rendering, animation, UI
- **Networking:** Netcode, Photon, Playfab
- **Performance:** Optimization tools, profiler

#### Unreal Engine
- **Language:** C++, Blueprints visual scripting
- **Graphics:** Nanite, Lumen advanced rendering
- **Performance:** Industry-leading graphics
- **Networking:** Replication Graph, advanced multiplayer
- **Use:** AAA games, realistic graphics

#### Godot
- **Language:** GDScript (Python-like)
- **Open Source:** Free, community-driven
- **Features:** 2D/3D, lightweight
- **Editor:** Intuitive node-based system
- **Use:** Indies, 2D games, low-spec games

## Mobile Game Development Path

### 1. Core Mechanics
- Movement & controls
- Collision detection
- Simple physics
- Game state management

### 2. Graphics & Animation
- Sprite rendering
- Sprite sheets & animation
- Particle effects
- Camera systems

### 3. Audio & Polish
- Sound effects
- Background music
- UI sounds
- Visual feedback (haptics)

### 4. Multiplayer (Optional)
- Client-server architecture
- State synchronization
- Latency compensation
- Matchmaking

### 5. Deployment
- Build optimization
- App store submission
- Analytics integration
- User feedback

## Platform-Specific Considerations

### iOS Specifics
- Safe Area layout
- Notch handling
- Home indicator
- App store review guidelines
- iOS app lifecycle

### Android Specifics
- Multiple screen sizes
- Back button handling
- Battery optimization
- Android manifest
- Play Store policies

### Game Platforms
- Xbox, PlayStation, Nintendo
- Steam, Epic Games Store
- Mobile app stores (iOS, Android)
- Web (WebGL, WebGPU)

## Performance Optimization

### Mobile Apps
- Lazy loading & pagination
- Image optimization
- Memory management
- Battery optimization
- Network efficiency

### Games
- Level of Detail (LOD)
- Frustum culling
- Batch rendering
- Texture atlasing
- Physics optimization

## Testing Strategies

### Mobile Apps
- Unit tests
- Widget/Component tests
- Integration tests
- UI automation tests
- Performance profiling

### Games
- Gameplay testing
- Performance testing
- Network testing
- Platform-specific testing
- User testing

## When to Use This Skill

### Mobile Development
- Building iOS/Android apps
- Cross-platform development
- Native performance needs
- Starting mobile journey
- Choosing platform/language

### Game Development
- Creating 2D/3D games
- Understanding game architecture
- Optimizing game performance
- Multiplayer implementation
- Publishing to stores

## Resources

- **React Native:** React Native docs, Expo
- **Flutter:** Flutter docs, pub.dev
- **Swift:** Apple Developer documentation
- **Kotlin:** Android Developers, Kotlin docs
- **Engines:** Unity Learn, Unreal Engine docs, Godot docs
- **Game Dev:** GameDev tutorials, OpenGL/Vulkan guides
