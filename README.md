# 📱 Practical 3 – Implicit & Explicit Intent

## 📌 Aim

**Create an Android application which demonstrates Implicit and Explicit Intent.**

This practical is developed as part of the **Mobile Application Development (MAD)** course. The application demonstrates how Android Intents are used to communicate between Activities and interact with other applications or system components.

---

## 🎯 Objectives

The main objectives of this practical are:

* Understand the concept of **Intent** in Android.
* Implement **Explicit Intent**.
* Implement **Implicit Intent**.
* Navigate from one Activity to another.
* Pass information between Activities using Intent.
* Open external applications using Implicit Intent.
* Understand how Android handles different Intent actions.

---

## 🛠️ Technologies Used

* **IDE:** Android Studio
* **Language:** Kotlin
* **UI:** XML
* **Platform:** Android
* **Build System:** Gradle

---

# 🔗 What is an Intent?

An **Intent** is a messaging object used in Android to request an action from another application component.

Intents can be mainly divided into two types:

1. **Explicit Intent**
2. **Implicit Intent**

---

# 1️⃣ Explicit Intent

An **Explicit Intent** is used when we know exactly which Activity or component we want to start.

For example, an application can use Explicit Intent to move from `MainActivity` to another Activity within the same application.

### Example

```kotlin
val intent = Intent(this, SecondActivity::class.java)
startActivity(intent)
```

Here:

* `this` represents the current Activity.
* `SecondActivity::class.java` specifies the Activity to be opened.
* `startActivity()` starts the new Activity.

### Flow

```text
MainActivity
     │
     │ Explicit Intent
     ↓
SecondActivity
```

---

# 2️⃣ Implicit Intent

An **Implicit Intent** does not specify a particular Activity or application.

Instead, it specifies an **action** that needs to be performed, and Android finds an appropriate application capable of handling that action.

For example, an Implicit Intent can be used to:

* Open a website
* Make a phone call
* Send an email
* Open a map
* Share information

### Example – Open Website

```kotlin
val intent = Intent(
    Intent.ACTION_VIEW,
    Uri.parse("https://www.google.com")
)
startActivity(intent)
```

Android identifies an application such as a web browser that can handle the `ACTION_VIEW` request.

### Flow

```text
Your Application
       │
       │ Implicit Intent
       ↓
Android System
       │
       ↓
Suitable Application
```

---

# 🔄 Difference Between Explicit and Implicit Intent

| Feature              | Explicit Intent             | Implicit Intent                    |
| -------------------- | --------------------------- | ---------------------------------- |
| Target               | Specific Activity/component | Suitable application/component     |
| Used for             | Navigation within an app    | Communication with other apps      |
| Component specified  | Yes                         | No                                 |
| Example              | Open SecondActivity         | Open browser                       |
| Selection by Android | Not required                | Android selects suitable component |

---

# 📱 Application Demonstration

The application demonstrates the use of both types of Intent.

### Explicit Intent

The application uses Explicit Intent to navigate between Activities.

```text
Activity 1
    ↓
Explicit Intent
    ↓
Activity 2
```

### Implicit Intent

The application uses Implicit Intent to perform an action using another application or Android system component.

```text
Current Activity
       ↓
Implicit Intent
       ↓
Android System
       ↓
Suitable Application
```

---

# 📂 Project Structure

```text
24012021039_practical3/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── ...
│           │
│           ├── res/
│           │   ├── drawable/
│           │   ├── mipmap/
│           │   ├── values/
│           │   └── layout/
│           │       └── ...
│           │
│           └── AndroidManifest.xml
│
├── gradle/
├── build.gradle.kts
├── gradle.properties
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
└── README.md
```

The repository currently contains the Android application module and standard Gradle project files.

---

# ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/jiyapatel02/24012021039_practical3.git
```

2. Open **Android Studio**.

3. Select **Open** and choose the cloned project folder.

4. Allow Gradle to sync.

5. Connect an Android device or start an Android Emulator.

6. Click the **Run ▶** button.

7. Test the Explicit and Implicit Intent functionality in the application.

---

# 🧪 Practical Testing

## Test 1 – Explicit Intent

**Action:** Click the button used for Activity navigation.

**Expected Result:**

```text
Current Activity
       ↓
Second Activity
```

The application opens the specified Activity.

---

## Test 2 – Implicit Intent

**Action:** Click the button associated with an external action.

**Expected Result:**

Android opens an appropriate application capable of handling the requested Intent.

For example:

```text
Application
    ↓
Implicit Intent
    ↓
Web Browser / Phone / Email / Other App
```

---

# 📚 Concepts Covered

| No. | Concept                            |
| --- | ---------------------------------- |
| 1   | Android Intent                     |
| 2   | Explicit Intent                    |
| 3   | Implicit Intent                    |
| 4   | Activity Navigation                |
| 5   | `startActivity()`                  |
| 6   | `Intent.ACTION_VIEW`               |
| 7   | URI Handling                       |
| 8   | Inter-Activity Communication       |
| 9   | Android System Components          |
| 10  | Communication Between Applications |

---

# 🎓 Learning Outcome

After completing this practical, we understand:

* What an Android Intent is.
* The difference between Explicit and Implicit Intent.
* How to navigate between Activities.
* How to start another Activity using Explicit Intent.
* How to launch external applications using Implicit Intent.
* How Android determines which application should handle an Implicit Intent.

---

# 👩‍💻 Author

**Jiya Patel**

**B.Tech – Information Technology**
**Mobile Application Development (MAD)**

---

## 🔗 GitHub Repository

[24012021039_practical3 – GitHub Repository](https://github.com/jiyapatel02/24012021039_practical3)

---

## ⭐ Conclusion

This practical provides a basic understanding of **Android Intents**. By implementing Explicit and Implicit Intents, the application demonstrates Activity navigation and communication with other Android applications and system components.
