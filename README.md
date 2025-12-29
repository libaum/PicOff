<div align="center">
  <h1>📸 Pic Off</h1>

  <p>
    <strong>Social Photo Challenge App for Android</strong>
  </p>

  <p>
    <a href="https://kotlinlang.org/"><img src="https://img.shields.io/badge/Language-Kotlin-7f52ff?style=flat-square&logo=kotlin" alt="Kotlin" /></a>
    <a href="https://developer.android.com/"><img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=flat-square&logo=android" alt="Android" /></a>
    <a href="https://firebase.google.com/"><img src="https://img.shields.io/badge/Backend-Firebase-FFCA28?style=flat-square&logo=firebase" alt="Firebase" /></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License" /></a>
  </p>
</div>

## 💡 About

**Pic Off** makes photo challenges fun and effortless. Built natively with **Kotlin**, it allows users to challenge friends to take the best picture based on a specific theme.

The goal was to engineer a robust **Single-Activity application** utilizing **MVVM architecture** to handle complex state transitions seamlessly.

---

## 📱 Screenshots

| Home & Feed | Challenges | Start New Challenge |
|:-----------:|:----------------:|:----------------:|
| <img src="assets/home.jpg" width="200" alt="Home Screen" /> | <img src="assets/challenges.jpg" width="200" alt="Create Screen" /> | <img src="assets/start_challenge.jpg" width="200" alt="Voting Screen" /> |
---

## 🛠 Tech Stack

* **Architecture:** MVVM, Single Activity (Navigation Component), ViewBinding
* **Core:** Kotlin, Coroutines, LiveData
* **Backend (Firebase):** Auth (Google Sign-In), Realtime Database, Storage
* **Key Features:** AlarmManager (Resilient Notifications), Camera Intents, Offline Support

---

## 🔄 Challenge State Logic

Managing the lifecycle of a challenge between two users is handled via a state machine in the `MainViewModel`:

```mermaid
graph LR
    A[Sent] --> B[Open]
    B --> C[Vote Recipient]
    C --> D[Vote Challenger]
    D --> E[Result]
    E --> F[Done]
```

1. **Sent:** Challenger sends request.
2. **Open:** Recipient accepts and uploads photo.
3. **Vote Recipient:** Recipient votes.
4. **Vote Challenger:** Challenger votes.
5. **Result:** Winner is calculated and displayed.
6. **Done:** Challenge completed.

---

## 📥 Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/libaum/PicOff.git
   ```

2. **Firebase Setup**
   * Add your own `google-services.json` to the `/app` directory.

3. **Build**
   * Open in **Android Studio** (Electric Eel+) and run (minSdk 26).

---

<p align="center">
    Built with ❤️ and Kotlin for Android
</p>