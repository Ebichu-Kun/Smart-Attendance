# Smart Attendance System

## 📌 About

**Smart Attendance System** is a web-based attendance application designed to make classroom attendance **faster, secure, and resistant to proxy attendance**.

Traditional attendance can take around **10–15 minutes** of class time when teachers manually call students' names and record their presence.

This application reduces that time by allowing students to mark their own attendance through a secure verification process.

The teacher starts an attendance session that is available for **only 2 minutes**. During this time, a student must successfully complete **all three verification methods**:

1. 📍 Be within the required proximity of the teacher/classroom.
2. 📷 Verify their face using the face registered with the application.
3. 🔢 Enter the temporary attendance code provided by the teacher.

Only when **all three conditions are successfully satisfied** will the student be marked present.

The short 2-minute window and multiple verification methods are designed to make **proxy attendance and cheating significantly more difficult**.

---

## ⚙️ How It Works

### 👨‍🏫 Teacher

The teacher logs into the application and starts an attendance session for the selected class.

```text
Teacher Login
     ↓
Select Class
     ↓
Start Attendance
     ↓
2-Minute Attendance Window
     ↓
Students Complete Verification
     ↓
Attendance Recorded
```

When the teacher starts the session, a **temporary attendance code** is generated.

The attendance session remains active for **2 minutes**. Once the time expires, students can no longer use that session to mark attendance.

---

### 👨‍🎓 Student

The student opens the active attendance session and completes the required verification steps.

#### 1. 📍 Proximity Verification

The system checks whether the student is within the required proximity of the teacher/classroom.

```text
Student Location
       ↓
Proximity Check
       ↓
Within Allowed Area?
    ↙          ↘
  YES           NO
   ↓             ↓
 Continue     Attendance
 Verification  Rejected
```

#### 2. 📷 Face Verification

The student's face is scanned and compared with the face previously registered with the application.

```text
Face Scan
    ↓
Compare With Registered Face
    ↓
Face Match?
  ↙      ↘
YES       NO
 ↓         ↓
Continue  Rejected
```

#### 3. 🔢 Attendance Code

The student enters the temporary code displayed/provided by the teacher.

The code is valid only for the current attendance session and becomes invalid when the session expires.

---

## ✅ Attendance Decision

The student is marked **Present only when all conditions are satisfied**.

```text
                 Attendance Session Active
                           ↓
                  Student Enrolled
                           ↓
                  Proximity Verified
                           ↓
                    Face Verified
                           ↓
                    Code Verified
                           ↓
                 Attendance Marked
                     PRESENT ✅
```

If any verification fails, attendance is **not marked**.

```text
Proximity ❌
     OR
Face ❌
     OR
Code ❌
     OR
Session Expired ❌
        ↓
Attendance Not Marked ❌
```

---

## ⏱️ Why the 2-Minute Window?

The attendance session is intentionally limited to **2 minutes**.

This helps prevent students from:

- Sharing an attendance code and marking attendance later.
- Reusing an old attendance code.
- Marking attendance after leaving the classroom.
- Giving another student enough time to complete the attendance process.
- Circumventing the attendance session after it has ended.

The short time window works together with **proximity verification and face verification** to provide multiple layers of protection against proxy attendance.

---

## 👨‍🏫 After Attendance

Once the 2-minute session expires, the teacher can view the attendance results.

The teacher can see:

- ✅ Students who are present
- ❌ Students who are absent

If a student experienced a genuine technical problem while completing the verification process, the teacher can manually mark that student as present from the absent-student list.

---

## 👨‍🎓 Student Attendance Tracking

Students can also view their own attendance records.

They can track:

- Attendance by date
- Present/absent status
- Total attendance
- Attendance percentage

This allows students to monitor their attendance without requiring the teacher to provide the records manually.

---

## 🎯 Main Objective

The main objective of the Smart Attendance System is to:

> **Reduce the time spent on classroom attendance while making proxy attendance significantly harder through time-limited, location-based, face-based, and code-based verification.**
