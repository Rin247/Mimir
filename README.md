# Mimir — Modern Android Keyboard with Full CJK & RTL Support

Mimir is an advanced, privacy-first Android input method (IME) keyboard built with Kotlin, Jetpack Compose, and Material 3 design. Designed specifically to solve high-friction script switching, Mimir features native support for complex CJK (Chinese, Japanese, Korean) input methods, right-to-left (RTL) scripts (Arabic, Hebrew, Persian, Urdu), and over 100 world languages with zero data collection or network permissions.

---

## ⌨️ Key Features & Module Breakdown

### 🌏 CJK Engine (`ime-cjk`)
- **Current**: Pinyin (Simplified & Traditional Chinese), Hiragana/Katakana Romaji input, and Hangul 2-Set Korean IME layouts with inline candidate selection bar.
- **Planned / Roadmap**: Cangjie, Zhuyin (Bopomofo), Wubi input methods, stroke recognition, and fast local candidate frequency adaptation.

### ✒️ RTL & Complex Script Engine (`ime-rtl`)
- **Current**: Full bidirectional text handling for Arabic, Persian, Urdu, and Hebrew with contextual letter shaping, diacritic toggles, and RTL-native layout reflow.
- **Planned / Roadmap**: Nastaliq font shaping optimization, ligature toggles, and HarfBuzz native shaping integration.

### 🎨 Customization & Theme Engine (`theme`)
- **Current**: Dynamic Material 3 color extraction, dark/light mode, custom key height, vibration feedback, and keypress sound effects.
- **Planned / Roadmap**: Custom background imagery, keycap styling engine, custom sound font support, and layout designer.

### 💡 Dictionary & Next-Word Prediction (`prediction`)
- **Current**: Local, offline N-gram word prediction and spell checking across 100+ languages.
- **Planned / Roadmap**: On-device AI transformer-based next-word completion, custom dictionary import/export, and user shorthand expansions.

### 📋 Clipboard & Gesture Toolbar (`toolbar`)
- **Current**: Pins, clipboard history, quick text insertion, number row toggle, and cursor movement gestures (spacebar swipe).
- **Planned / Roadmap**: Multi-item clipboard manager, floating split keyboard for foldables/tablets, and voice input integration.

---

## 🏗️ Architecture & Technology Stack

- **Platform**: Android 13+ (minSdk 33, targetSdk 37).
- **UI & Input**: Kotlin, Jetpack Compose, Android IME (`InputMethodService`).
- **Privacy Contract**: Zero INTERNET permission required; all candidate processing remains 100% on-device.
- **Licensing**: AGPL-3.0.

---

## 🛠️ Building & Running

### Prerequisites
- **Android Studio** (2026.2.2+) or Gradle CLI
- **JDK 25**

### Build Commands

```bash
# Build Debug APK
./gradlew assembleDebug

# Install IME on connected device
./gradlew installDebug
```

---

## 📜 License

Mimir is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
