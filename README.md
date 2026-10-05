# 📱 MAD Practical-2 — Activity Life Cycle and Basic UI

This repository contains the implementation of **Practical-2** for the **Mobile Application Development (MAD)** subject.

The practical demonstrates the **Android Activity Life Cycle** and basic Android UI components using **Kotlin, XML, TextView, Toast, Snackbar, Logcat, and ConstraintLayout**.

---

## 📌 Practical Information

| Information    | Details                              |
| -------------- | ------------------------------------ |
| **Subject**    | Mobile Application Development (MAD) |
| **Practical**  | Practical-2                          |
| **Language**   | Kotlin                               |
| **UI**         | XML                                  |
| **IDE**        | Android Studio                       |
| **Layout**     | ConstraintLayout                     |
| **Repository** | 24012021068_MAD_Parctical2           |

---

## 🎯 Aim

To create an Android application that demonstrates the functions of the **Activity Life Cycle** and **Basic UI** using:

* TextView
* Toast
* Snackbar
* Log messages
* Logcat
* ConstraintLayout

The application displays **"Hello World"** in the center of the Activity screen with the specified text and layout properties.

---

## 🎯 Objectives

The objectives of this practical are:

* Display **Hello World** using a `TextView`.
* Apply basic UI properties to the `TextView`.
* Understand and implement `ConstraintLayout`.
* Understand the Android Activity Life Cycle.
* Implement Activity Life Cycle callback methods.
* Display lifecycle events in Logcat.
* Display Toast messages.
* Display Snackbar messages.
* Understand Android built-in color resources.
* Generate and use a unique ID for a `TextView`.

---

## 🛠️ Technologies Used

* **Android Studio**
* **Kotlin**
* **XML**
* **ConstraintLayout**
* **Android SDK**
* **Logcat**
* **Git**
* **GitHub**

---

# 🎨 Basic UI Design

The application contains a `TextView` with the following properties:

| Property       | Value            |
| -------------- | ---------------- |
| **Text**       | `Hello World`    |
| **Background** | Yellow `#FFFF00` |
| **Text Color** | Holo Blue Bright |
| **Text Size**  | `27sp`           |
| **Text Style** | Bold + Italic    |
| **Alignment**  | Center           |
| **Layout**     | ConstraintLayout |

### TextView XML

```xml
<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello World"
    android:textColor="@android:color/holo_blue_bright"
    android:textSize="27sp"
    android:textStyle="bold|italic"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
```

The Activity layout uses a yellow background:

```xml
android:background="#FFFF00"
```

---

# 🔄 Activity Life Cycle

Android Activities have several important lifecycle callback methods.

This practical demonstrates:

1. `onCreate()`
2. `onStart()`
3. `onResume()`
4. `onPause()`
5. `onStop()`
6. `onRestart()`
7. `onDestroy()`

Each lifecycle method generates a message that can be observed in **Android Studio Logcat**.

---

## 🔁 Activity Life Cycle Flow

```text
              onCreate()
                   ↓
               onStart()
                   ↓
              onResume()
                   ↓
          Activity Running
                   ↓
               onPause()
                   ↓
               onStop()
                   ↓
          ┌────────┴────────┐
          ↓                 ↓
     onRestart()       onDestroy()
          ↓
       onStart()
          ↓
       onResume()
```

---

# 📝 Log Messages

`Log.d()` is used to display Activity Life Cycle events in Android Studio's **Logcat**.

Example:

```kotlin
Log.d("ActivityLifeCycle", "onCreate called")
```

Similar messages are generated for the other lifecycle methods.

Example output:

```text
onCreate called
onStart called
onResume called
```

---

# 🍞 Toast Messages

A **Toast** displays a short message to the user.

Example:

```kotlin
Toast.makeText(
    this,
    "onCreate called",
    Toast.LENGTH_SHORT
).show()
```

Toast messages are used to demonstrate when different Activity Life Cycle methods are executed.

---

# 📢 Snackbar Messages

A **Snackbar** displays a short message at the bottom of the screen.

Example:

```kotlin
Snackbar.make(
    findViewById(android.R.id.content),
    "onResume called",
    Snackbar.LENGTH_SHORT
).show()
```

Snackbar messages provide visual feedback when lifecycle events occur.

---

# 📱 Application Output

## Main Activity

The application displays:

### **Hello World**

with the following properties:

* Yellow background
* Holo Blue Bright text
* 27sp text size
* Bold and Italic text
* Center alignment

---

## Logcat Output

When the Activity is launched, the following lifecycle messages can be observed:

```text
onCreate called
onStart called
onResume called
```

When the Activity is paused or stopped:

```text
onPause called
onStop called
```

When the Activity is opened again:

```text
onRestart called
onStart called
onResume called
```

---

# 🧪 Practical Demonstration

The Activity Life Cycle can be observed using the following actions.

### 1. Launch Application

```text
onCreate()
onStart()
onResume()
```

### 2. Press Home Button

```text
onPause()
onStop()
```

### 3. Open Application Again

```text
onRestart()
onStart()
onResume()
```

### 4. Close Activity

```text
onPause()
onStop()
onDestroy()
```

> **Note:** The exact lifecycle callbacks may vary depending on how the Activity is closed and how Android manages the application process.

---

# 📚 Concepts Covered

This practical covers the following Android and Kotlin concepts:

* TextView
* TextView properties
* Text size
* Text style
* Text color
* Android built-in color resources
* ConstraintLayout
* Layout background
* View IDs
* Toast messages
* Snackbar messages
* Log messages
* Logcat
* Activity Life Cycle
* Activity states
* Kotlin
* XML layouts

---

# 📂 Project Structure

```text
24012021068_MAD_Parctical2/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── ...
│           │
│           ├── res/
│           │   ├── drawable/
│           │   ├── layout/
│           │   │   └── activity_main.xml
│           │   │
│           │   └── values/
│           │
│           └── AndroidManifest.xml
│
├── gradle/
│
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

---

# ▶️ How to Run

### Step 1 — Clone the Repository

```bash
git clone https://github.com/Sakariya-Krish/24012021068_MAD_Parctical2.git
```

### Step 2 — Open in Android Studio

Open the cloned project in **Android Studio**.

### Step 3 — Gradle Sync

Allow Android Studio to complete the **Gradle synchronization**.

### Step 4 — Connect Device

Connect an Android phone with USB Debugging enabled or start an Android Emulator.

### Step 5 — Run Application

Click:

```text
Run ▶
```

### Step 6 — Observe the Application

The application will display **Hello World** in the center of the screen.

### Step 7 — Check Logcat

Open **Logcat** in Android Studio and filter using:

```text
ActivityLifeCycle
```

You can observe the Activity Life Cycle events as they occur.

---

# 🎓 Learning Outcomes

After completing this practical, the following concepts are understood:

* Android Activity Life Cycle
* Activity states
* `onCreate()`
* `onStart()`
* `onResume()`
* `onPause()`
* `onStop()`
* `onRestart()`
* `onDestroy()`
* Basic Android UI
* ConstraintLayout
* TextView
* Toast
* Snackbar
* Logcat
* Kotlin Activity programming
* XML-based UI design

---

# 📌 Conclusion

MAD Practical-2 provides an understanding of the **Android Activity Life Cycle** and basic UI development.

The practical demonstrates how an Activity moves through different lifecycle states and how these events can be monitored using **Logcat, Toast, and Snackbar messages**. It also provides basic experience with designing Android interfaces using **ConstraintLayout and TextView**.

---

## 👨‍💻 Author

**Krish Sakariya**

**Course:** B.Tech Information Technology
**Subject:** Mobile Application Development (MAD)
