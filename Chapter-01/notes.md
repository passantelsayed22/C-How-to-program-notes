## 1.1 Introduction to C

### C Language
- C is one of the oldest widely used programming languages.
- It is widely used in industry and systems programming.
- Major operating systems such as Windows, macOS, and Linux contain significant amounts of C code.
- Many widely used applications and database systems also contain C code.

### Software vs Hardware
- **Hardware**: The physical components of a computer and its connected devices.
- **Software**: The instructions/programs that tell the hardware what to do.
- Programmers write software by creating ordered instructions that the computer executes.

---

## 1.2 Hardware and Software

- Modern computers can perform billions of operations per second.
- Supercomputers can perform vastly more operations per second.
- Silicon chips made modern computing devices much smaller and less expensive.
- Silicon is abundant in nature and is a major component of sand.

### Moore's Law
- Moore's Law describes the historical trend that processor capability approximately doubled about every two years while the cost per capability decreased.
- The trend has influenced improvements in:
  - Memory capacity
  - Secondary storage capacity
  - Processor speeds
- The traditional scaling described by Moore's Law has become increasingly difficult to maintain.
- Modern performance improvements increasingly rely on architectural techniques such as **multicore processors**.

### Embedded Systems
- An **embedded system** is a computer system built into a larger device to perform specific functions.
- Examples include:
  - Smart home devices
  - Security systems
  - Robots
  - Smart traffic systems

### Bandwidth
- **Bandwidth** is the amount of data that can be transmitted over a communication channel in a given amount of time.
- Improvements in communication technology and reduced communication costs contributed to the **Information Revolution**.

---

## 1.2.2 Computer Organization

A computer can be viewed as a collection of major functional units:

### 1. Input Unit
Receives data and instructions from outside the computer.

Examples:
- Keyboard
- Mouse
- Touchscreen
- Microphone / voice input
- Camera
- Barcode reader
- Internet data
- GPS data
- Accelerometer data
- Data read from secondary storage
  - USB flash drives
  - Blu-ray discs

**Important:** Receiving data from the Internet or reading data from storage is also considered input.

---

### 2. Output Unit
Presents processed information to the outside world.

Examples:
- Displays/screens
- Printed documents
- Audio
- Video
- Data transmitted over the Internet
- Signals controlling other devices
- Game-controller vibrations
- VR/AR devices

---

### 3. Memory Unit
- Stores data and instructions that are currently being used.
- Main memory is typically **RAM (Random Access Memory)**.
- RAM is **volatile memory**: its contents are lost when power is removed.
- A byte consists of **8 bits**.
- A bit represents a binary value: **0 or 1**.

---

### 4. Arithmetic and Logic Unit (ALU)
Performs:
- Arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division
- Logical operations and comparisons.

The ALU is integrated into modern CPUs.

---

### 5. Central Processing Unit (CPU)
- The CPU coordinates and controls the activities of the computer.
- It directs data movement between the input unit, memory, ALU and output unit.
- Modern CPUs commonly contain multiple processing cores.

---

### 6. Secondary Storage
- Provides long-term, persistent storage for programs and data.
- Unlike RAM, its contents remain after power is removed.
- It is generally slower than RAM but provides much larger storage capacity at lower cost.

Examples:
- Hard Disk Drives (HDDs)
- Solid-State Drives (SSDs)
- USB flash drives

---

## Multicore Processors

### Core
- A **core** is an individual processing unit within a processor.

### Multicore Processor
- A multicore processor contains multiple processing cores on a single chip.
- Multiple cores can execute tasks concurrently, allowing greater overall processing capability.

Examples:
- Dual-core → 2 cores
- Quad-core → 4 cores
- Octa-core → 8 cores

### Why Multicore?
Increasing the clock speed of a single core produces problems such as:
- Higher power consumption
- Increased heat generation
- Physical limitations of transistor scaling

Using multiple cores provides another way to increase overall processing performance without relying entirely on increasing the speed of one core.

### Multithreading
- **Multithreading** allows a program to divide work into multiple threads.
- Threads can potentially execute concurrently on different CPU cores.
- The operating system schedules and distributes tasks among available cores.

---

## Important Engineering Connections

### Electron Leakage and Transistor Scaling
- As transistors become extremely small, physical effects become increasingly important.
- **Quantum tunneling** can allow electrons to pass through barriers that would normally prevent them from crossing.
- Leakage increases unwanted power consumption and heat.
- These physical limitations are among the challenges that make continued traditional transistor scaling difficult.

### CPU Cache
- Modern processors use very fast **cache memory** to reduce the time needed to access frequently used data and instructions.
- Common cache levels include **L1, L2 and L3**.
- L1/L2 are generally closer to individual cores, while L3 is typically shared across multiple cores.

### RAM vs Secondary Storage
| RAM | Secondary Storage |
|---|---|
| Volatile | Persistent |
| Faster | Generally slower |
| Smaller capacity | Much larger capacity |
| Used for active data/programs | Used for long-term storage |
| Data lost when power is removed | Data remains after power is removed |

## Data Hierarchy & Big Data

- **Metadata** = بيانات تصف بيانات أخرى.
  - مثال: التغريدة نفسها محتوى، لكن وقت النشر، الجهاز، الموقع، وغيرها تعتبر Metadata.
  - Metadata مهمة جدًا في **Data Mining** وتحليل سلوك المستخدمين.

- **Data Mining** = استخراج patterns / relationships / predictions من كميات كبيرة من البيانات.

- **Relational Database**
  - البيانات بتتخزن في Tables مرتبطة ببعض.
  - غالبًا بنستخدم **IDs / Keys** لربط الجداول بدل تكرار نفس البيانات.
  - ده يقلل **data redundancy** ويسهّل إدارة البيانات.

- **1024 = 2¹⁰**
  - السبب إن أنظمة الكمبيوتر مبنية على Binary.
  - ملاحظة: في الاستخدام الحديث فيه فرق بين:
    - **KB = 1000 bytes** (النظام العشري)
    - **KiB = 1024 bytes** (النظام الثنائي)

---

## Programming Languages

- **Machine Language is architecture-dependent**
  - كل CPU architecture عندها **Instruction Set** مختلف.
  - لذلك نفس Machine Code لا يعمل بالضرورة على معمارية مختلفة مثل **x86** و **ARM**.

- **Compiler vs Interpreter**
  - Compiler: يحوّل البرنامج إلى شكل قابل للتنفيذ قبل التشغيل.
  - Interpreter: ينفذ التعليمات أثناء التشغيل.
  - بعض اللغات تستخدم **Hybrid approach**.

- **JIT (Just-In-Time Compilation)**
  - الكود يتحول إلى Machine Code أثناء الـ Runtime بدل ما يكون كل التحويل قبل التشغيل.
  - مثال مهم: **C# / .NET** → Source Code → Intermediate Language → JIT → Machine Code.

- **Portability ≠ Machine independence بالكامل**
  - High-level languages أسهل في نقلها بين الأجهزة، لكن الـ compiler/runtime والـ platform ممكن يؤثروا على portability.

---

## Operating Systems

- **Kernel** هو الجزء الأساسي من الـ Operating System والمسؤول عن التعامل مع موارد الجهاز مثل:
  - CPU
  - Memory
  - Devices
  - Processes

- **Open Source ≠ أي شخص يقدر يعدّل النسخة الأصلية مباشرة**
  - أي شخص يقدر يشوف ويعدل ويعمل نسخة من الكود حسب الـ License.
  - التعديلات على المشروع الأساسي عادةً تمر عبر:
    **Fork → Changes → Pull Request → Code Review → Tests → Merge**

- **macOS ليس Linux**
  - الاتنين من عائلة Unix-like systems، لكن macOS مبني على **Darwin** وليس Linux.
  - Darwin يحتوي على مكونات مفتوحة المصدر مثل **XNU kernel + BSD components**.
  - أجزاء كبيرة من macOS نفسه Closed Source.

- **macOS و Linux**
  - اشتراكهم في Unix/POSIX-style environment هو أحد أسباب تشابه أوامر الـ Terminal مثل:
    `ls`, `cd`, `cp`, `mv`

---

## Apple & Mobile Development

- **NeXTSTEP → macOS**
  - Apple اشترت NeXT سنة 1996.
  - تقنيات NeXTSTEP أصبحت أساسًا مهمًا لنظم Apple الحديثة.
  - لذلك أسماء مثل `NSString` و `NSArray` مرتبطة تاريخيًا بـ NeXT.

- **Swift**
  - Swift أصبحت Open Source سنة 2015.
  - يمكنها التفاعل مع كود مكتوب بـ **C / Objective-C**.

- **Native Code**
  - في تطبيقات الموبايل، ممكن نستخدم C/C++ للأجزاء التي تحتاج Performance عالي.
  - Android يوفر **NDK (Native Development Kit)** لهذا النوع من التطوير.

---

## IoT & Embedded Systems

- **IoT** = أجهزة Computing متصلة ببعضها أو بالإنترنت لتبادل البيانات وتنفيذ وظائف ذكية.

- **Embedded System**
  - Computer system مخصص لوظيفة محددة داخل جهاز أكبر.
  - أمثلة: سيارات، أجهزة طبية، ATMs، أجهزة منزلية، أنظمة تحكم.

- الفرق المهم:
  - **Computer عام** → ينفذ مهام كثيرة.
  - **Embedded System** → غالبًا مصمم لمهمة أو مجموعة مهام محددة.

- **C** مهمة جدًا في Embedded Systems لأنها تسمح بتحكم منخفض المستوى في:
  - Memory
  - Hardware
  - Registers
  - CPU

---

## C Language

- تاريخ C:
  **BCPL → B → C**
  
- **Dennis Ritchie** طوّر C سنة 1972 في Bell Labs.

- C تجمع بين:
  - High-level programming features
  - Low-level hardware control

- **C is portable but not completely hardware-independent**
  - نفس Source Code يمكن نقله بين منصات مختلفة، لكن غالبًا يحتاج **Compiler مناسب** وقد يحتاج تعديلات حسب الـ hardware/OS.

- **Standardization**
  - ANSI/ISO standards تحدد سلوك اللغة وقواعدها بحيث يكون الكود أكثر قابلية للنقل بين Compilers المختلفة.

### Real-Time Systems

- **Real-Time System** مش معناه "سريع" فقط.
- الأهم إنه يعطي **predictable response within a required time limit**.

- **Hard Real-Time**
  - تجاوز الـ deadline قد يؤدي لفشل خطير.
  - مثال: بعض أنظمة التحكم الحرجة.

- **Soft Real-Time**
  - التأخير غير مرغوب لكنه لا يعني بالضرورة كارثة.

---

## Software Reuse & Libraries

- **Software Reuse**
  - استخدام code/components موجودة ومختبرة بدل إعادة بنائها من الصفر.

- الفكرة الأساسية:
  **Don't reinvent the wheel.**

- استخدام Libraries يوفر:
  - Development time
  - Testing effort
  - Maintenance effort

- لكن قبل استخدام Open-Source Library لازم نراجع:
  - Documentation
  - License
  - Security
  - Maintenance status
  - Dependencies
  - Community / reliability

- **Library ≠ Framework**
  - Library: أنتِ تستدعيها وقت ما تحتاجيها.
  - Framework: هو الذي يحدد جزءًا كبيرًا من structure وflow الخاص بالتطبيق، وغالبًا يستدعي كودك.

- **Building Blocks**
  - البرنامج الكبير غالبًا بيتبني من:
    - Standard Libraries
    - Third-party/Open-Source Libraries
    - Reusable components
    - Functions written by the developer

---

## Important Engineering Connections

- **Open Source** مش معناه بالضرورة "مجاني بدون شروط".
  - الـ License تحدد إيه المسموح لك تعمليه بالكود.

- **Performance vs Productivity**
  - Low-level languages تعطي تحكمًا وأداءً أكبر.
  - High-level languages تعطي abstraction وإنتاجية أعلى.
  - الاختيار يعتمد على طبيعة الـ system والـ requirements.

- **Abstraction**
  - من أهم أفكار Computer Science:
  - إخفاء التفاصيل منخفضة المستوى وتوفير interface أبسط للمستخدم/المبرمج.
  - Libraries والـ Operating Systems والـ High-Level Languages كلها أمثلة على استخدام الـ abstraction.
 

    


## لغات البرمجة 🧩

الفكرة الأساسية:

> مفيش لغة أحسن مطلقًا؛ كل لغة مناسبة لنوع معين من المشروعات.

| اللغة | أهم استخدام / ميزة |
|---|---|
| **C / C++** | سرعة عالية + تحكم قريب من الـ Hardware |
| **Python** | سهلة + AI + Data Science + مكتبات ضخمة |
| **Java** | تطبيقات المؤسسات والسيرفرات + JVM |
| **C#** | تطبيقات وأنظمة متنوعة، خصوصًا بيئة Microsoft |
| **JavaScript** | تفاعل الويب، ومع Node.js تشتغل خارج المتصفح |
| **Swift** | تطبيقات Apple |
| **R** | Statistics و Data Analysis |
| **BASIC** | تعليم المبتدئين، والإصدارات الحديثة تدعم OOP |

### أهم الأفكار

- **Java → JVM → Write Once, Run Anywhere**
- **JavaScript → Browser + Node.js**
- **Python → واجهة سهلة + مكتبات كثيرة تعتمد في أجزاء أساسية منها على C/C++**

---

## رحلة الكود من الكتابة للتشغيل ⚙️

أهم سلسلة في الشابتر:

**Edit → Preprocess → Compile → Link → Load → Execute**

### Edit

المبرمج يكتب الكود ويحفظه، مثلًا:

```text
program.c
```

### Preprocess

الـ **Preprocessor** ينفذ التعليمات التي تبدأ بـ `#`، مثل:

```c
#include <stdio.h>
```

ويجهز الكود قبل مرحلة الـ Compilation.

### Compile

الـ **Compiler** يحول كود C إلى **Object Code**.

لو فيه خطأ في قواعد اللغة، يظهر:

```text
Syntax Error
Compilation Error
```

### Link

الـ **Linker** يربط الـ Object Code بالدوال الموجودة في المكتبات الخارجية، وينتج البرنامج القابل للتشغيل.

في بعض بيئات Unix/Linux يكون الاسم الافتراضي:

```text
a.out
```

### Load

الـ **Loader** ينقل البرنامج من الـ Disk إلى الـ Main Memory (RAM).

### Execute

الـ CPU يبدأ تنفيذ التعليمات.

ممكن تظهر أخطاء أثناء التشغيل مثل:

```text
Runtime Error
```

ومن أمثلتها:

```text
Divide by Zero
```

---

## Streams 📥📤

البرنامج بيتعامل مع 3 Streams أساسية:

```text
stdin   → Standard Input
stdout  → Standard Output
stderr  → Standard Error
```

عادةً:

```text
stdin  → Keyboard
stdout → Screen
stderr → Error messages
```

لكن ممكن إعادة توجيه الـ Streams بحيث البيانات تيجي من File أو مصدر آخر.

---

## بيئات تطوير C 💻

الكتاب ذكر:

```text
Windows → Visual Studio
macOS   → Xcode / Clang
Linux   → GCC
```

وفي الـ Terminal ممكن استخدام:

```bash
gcc -std=c18 program.c
./a.out
```

---

## Project و Solution

في Visual Studio:

```text
Project
↓
مجموعة ملفات تخص برنامج معين

Solution
↓
مجموعة Projects
```

---

## Guess Number Game 🎯

اللعبة تعتمد على تخمين رقم بين:

```text
1 → 1000
```

والفكرة مرتبطة بمفهوم:

```text
Binary Search
```

لأننا في كل محاولة بنقسم نطاق البحث تقريبًا إلى النصف.

عدد المحاولات القصوى تقريبًا:

```text
log₂(1000) ≈ 10
```

---

## الإنترنت والويب 🌐

### ARPANET

في أواخر الستينات ظهرت:

```text
ARPA
↓
ARPANET
↓
Internet
```

وكان الهدف الأساسي ربط أجهزة الكمبيوتر في الجامعات ومراكز الأبحاث.

---

## TCP/IP

### TCP

يقسم البيانات إلى أجزاء صغيرة:

```text
Data
↓
Packets
↓
Transmission
↓
Reassembly
```

ويضمن وصولها بالترتيب الصحيح.

### IP

يعطي الأجهزة عناوين تساعد الشبكات على معرفة مكان إرسال البيانات.

```text
IP Address
```

### TCP/IP

الاتنين مع بعض يشكلوا أساسًا مهمًا من أساسيات الاتصال عبر الإنترنت.

---

## Internet vs Web

### Internet

هو البنية التحتية:

```text
Cables
Routers
Servers
Networks
```

### World Wide Web

هو الخدمات والصفحات والمواقع التي تعمل فوق الإنترنت.

---

## Tim Berners-Lee

سنة:

```text
1989
```

طوّر الـ **World Wide Web** في CERN.

ومن أهم التقنيات المرتبطة بالويب:

```text
HTML
HTTP
```

### HTML

تستخدم لبناء صفحات الويب والروابط.

### HTTP

بروتوكول لنقل بيانات الويب.

### W3C

منظمة تهدف إلى وضع معايير للويب تساعد التقنيات والمتصفحات على العمل بطريقة متوافقة.

---

## Cloud Computing ☁️

بدل ما تكون كل الموارد على جهازك، ممكن تعتمد على موارد موجودة عبر الإنترنت.

مثل:

```text
Computing Power
Storage
Databases
Software
```

ومن نماذج:

```text
SaaS → Software as a Service
PaaS → Platform as a Service
IaaS → Infrastructure as a Service
```

---

## Mashups 🧩

فكرة الـ **Mashups** هي دمج أكثر من Web Service أو مصدر بيانات لبناء تطبيق جديد.

مثال:

```text
Real Estate Data
+
Maps Service
↓
Application
```

بدل بناء كل شيء من الصفر.

---

## Internet of Things — IoT 📡

الـ IoT هو ربط الأشياء والأجهزة بالشبكات بحيث تستطيع إرسال واستقبال البيانات.

أمثلة:

```text
Smart Sensors
Smart Meters
Temperature Sensors
Medical Devices
Tracking Devices
```

الفكرة:

```text
Thing
↓
Network
↓
Data
↓
System
```

---

## Software Technologies 🛠️

### Refactoring

تعديل وتنظيم الكود بدون تغيير وظيفته الأساسية.

الهدف:

```text
Cleaner Code
Easier Maintenance
Better Readability
```

مثال:

```text
Large Function
↓
Smaller Functions
↓
Cleaner Code
```

---

### Design Patterns

حلول وتصميمات مجربة لمشاكل برمجية متكررة.

الفكرة:

```text
Repeated Problem
↓
Known Pattern
↓
Reusable Solution
```

---

### SDK

اختصار:

```text
Software Development Kit
```

وهي مجموعة أدوات وDocumentation تساعد المبرمج على بناء تطبيقات لبيئة معينة.

مثال:

```text
iOS SDK
```

---

## Big Data 📊

البيانات أصبحت ضخمة جدًا من حيث الحجم والسرعة والتنوع.

وحدات قياس البيانات:

```text
Byte
↓
Kilobyte (KB)
↓
Megabyte (MB)
↓
Gigabyte (GB)
↓
Terabyte (TB)
↓
Petabyte (PB)
↓
Exabyte (EB)
↓
Zettabyte (ZB)
```

تقريبًا:

```text
1 KB ≈ 2¹⁰ Bytes
1 MB ≈ 2²⁰ Bytes
1 GB ≈ 2³⁰ Bytes
1 TB ≈ 2⁴⁰ Bytes
```

وبالنسبة للوحدات الكبيرة:

```text
1 PB = 1000 TB
1 EB = 1000 PB
1 ZB = 1000 EB
```

---

## Memory Limits 🧠

في Problem Solving ممكن تلاقي:

```text
Memory Limit: 256 MB
```

مثال:

لو عندنا:

```text
100,000,000 integers
```

والـ `int` حجمه:

```text
4 Bytes
```

فالمصفوفة تحتاج:

```text
100,000,000 × 4
= 400,000,000 Bytes
```

أي حوالي:

```text
400 MB
```

وده أكبر من:

```text
256 MB
```

وبالتالي ممكن يحصل:

```text
Memory Limit Exceeded
```

---

## Big Data Analytics 📈

مصطلح:

```text
Data Analysis
```

ظهر في وقت مبكر من تاريخ الحوسبة، بينما مصطلح:

```text
Big Data
```

ظهر لاحقًا مع زيادة حجم البيانات.

---

## The Four V's of Big Data

### Volume

حجم البيانات.

```text
How much data?
```

### Velocity

سرعة إنتاج البيانات وحركتها وتغيرها.

```text
How fast?
```

### Variety

تنوع أنواع البيانات.

مثل:

```text
Text
Images
Videos
Audio
Sensor Data
```

### Veracity

مدى صحة وموثوقية البيانات.

```text
Can we trust the data?
```

---

## Moore's Law ⚡

قانون مور ارتبط بتطور قدرات المعالجة وزيادة كثافة الترانزستورات مع مرور الوقت.

الفكرة العامة:

```text
Hardware Power
↑
Cost per computation
↓
```

وده ساعد على تخزين ومعالجة كميات ضخمة من البيانات بتكلفة أقل.

---

## Insight 🧠

الفكرة المهمة التي ذكرها الكتاب:

> الهدف من الحوسبة ليس مجرد الحصول على أرقام، وإنما الوصول إلى فهم وInsight مفيد.

يعني:

```text
Raw Data
↓
Processing
↓
Analysis
↓
Insight
↓
Decision
```

---

## Big Data Opportunities 🚀

الزيادة الكبيرة في البيانات أدت إلى فرص كثيرة في مجالات مثل:

```text
Artificial Intelligence
Machine Learning
Natural Language Processing
Data Science
```

---

## Big Data Use Cases 🌍

### Healthcare

```text
Cancer Diagnosis
Brain Mapping
Electronic Health Records
Medical Device Monitoring
```

### Security

```text
Fraud Detection
Cybersecurity
Threat Detection
```

### AI & NLP

```text
Machine Translation
Text Summarization
Emotion Detection
Sentiment Analysis
```

### Smart Cities

```text
Self-Driving Cars
Smart Traffic
Smart Homes
Ride-Sharing
```

---

## FLOPS ⚡

اختصار:

```text
Floating-Point Operations Per Second
```

ويستخدم لقياس عدد عمليات الـ Floating Point التي يستطيع النظام تنفيذها في الثانية.

تطور الأداء وصل إلى مستويات ضخمة مثل:

```text
GFLOPS
TFLOPS
PFLOPS
EFLOPS
```

---

## Quantum Computers ⚛️

الـ Quantum Computers مجال ما زال قيد التطوير.

تعتمد على مبادئ الحوسبة الكمية، وقد توفر قدرات كبيرة جدًا لبعض أنواع المسائل.

ومن أسباب الاهتمام بها:

```text
Cryptography
Optimization
Simulation
```

---

## AI 🤖

الذكاء الاصطناعي يهدف إلى بناء أنظمة تستطيع تنفيذ مهام تتطلب عادةً قدرات ذكية.

ومن الأهداف بعيدة المدى:

```text
AGI
```

أي:

```text
Artificial General Intelligence
```

وهو مفهوم يشير إلى نظام يمتلك قدرات عامة ومرنة في أداء مهام ذكية متعددة.

---

## AI Timeline 🧠

### Deep Blue — 1997

IBM's:

```text
Deep Blue
```

هزم بطل العالم في الشطرنج.

واعتمد بدرجة كبيرة على البحث المكثف في احتمالات النقلات.

---

### Watson — 2011

IBM's:

```text
Watson
```

فاز في:

```text
Jeopardy!
```

واستخدم تقنيات مرتبطة بـ:

```text
Natural Language Processing
```

للتعامل مع كميات ضخمة من المعلومات.

---

### AlphaGo — 2015

Google's:

```text
AlphaGo
```

استخدم:

```text
Deep Learning
Neural Networks
```

لعب لعبة Go والتفوق على لاعب محترف.

---

### AlphaZero

نظام:

```text
AlphaZero
```

استخدم:

```text
Reinforcement Learning
```

وتعلم اللعب من خلال التجربة بدل الاعتماد على تعليم بشري مباشر لخطط اللعب.

---

## Brute Force vs Algorithms

الـ Brute Force يحاول عددًا كبيرًا من الاحتمالات.

```text
Problem
↓
Try Many Possibilities
↓
Find Solution
```

لكن المشكلة أن عدد الاحتمالات قد يصبح ضخمًا جدًا.

لذلك نحتاج:

```text
Better Algorithms
+
Better Hardware
```

---

# 🧠 الصورة الكبيرة للشابتر

كل الأفكار السابقة مرتبطة ببعضها:

```text
Programming Languages
        ↓
Writing Code
        ↓
Edit
        ↓
Preprocess
        ↓
Compile
        ↓
Link
        ↓
Load
        ↓
Execute
        ↓
Operating Systems
        ↓
Networks
        ↓
Internet
        ↓
Web
        ↓
Cloud
        ↓
IoT
        ↓
Big Data
        ↓
Data Analytics
        ↓
Artificial Intelligence
        ↓
Machine Learning
        ↓
Future Computing
```

الفكرة الأساسية للشابتر:

> الكمبيوتر مش مجرد جهاز بنكتب عليه كود؛ هو منظومة كاملة تبدأ من لغة البرمجة، وتمر بالـ Compiler والـ Hardware والـ Operating System والشبكات، وتوصل في النهاية إلى Cloud وBig Data وAI.

