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

### أهم 3 أفكار

- **Java → JVM → Write Once, Run Anywhere**
- **JavaScript → Browser + Node.js**
- **Python → واجهة سهلة + مكتبات كثيرة تعتمد في أجزاء أساسية منها على C/C++**

---

# رحلة الكود من الكتابة للتشغيل ⚙️

أهم سلسلة في الشابتر:

**Edit → Preprocess → Compile → Link → Load → Execute**

### 1️⃣ Edit

المبرمج يكتب الكود ويحفظه، مثلًا:

```text
program.c
### 1️⃣ Edit
المبرمج يكتب الكود ويحفظه، مثلًا:
```text
program.c

⸻

2️⃣ Preprocess

الـ Preprocessor ينفذ أوامر خاصة قبل عملية الـ Compile.

مثال:

#include <stdio.h>

الأوامر التي تبدأ بـ # تسمى Preprocessor Directives.

⸻

3️⃣ Compile

الـ Compiler يحول الـ Source Code إلى Object Code.

وفي هذه المرحلة يمكن اكتشاف أخطاء الـ Syntax.

مثال:

printf("Hello")

نسيان ; قد يؤدي إلى:

Compilation Error

⸻

4️⃣ Link

الـ Linker يربط الـ Object Code بالمكتبات والـ Functions المطلوبة.

Object Code
     +
Libraries
     ↓
Executable

⸻

5️⃣ Load

الـ Loader ينقل البرنامج من الـ Disk إلى الـ Main Memory (RAM) حتى يصبح جاهزًا للتنفيذ.

Disk
 ↓
RAM

⸻

6️⃣ Execute

الـ CPU يبدأ في تنفيذ تعليمات البرنامج.

وهنا يمكن أن تحدث Runtime Errors.

مثال:

int x = 10 / 0;

⸻

🚨 أنواع الأخطاء المهمة

Syntax / Compile Error

خطأ في قواعد كتابة اللغة ويظهر أثناء الـ Compilation.

Runtime Error

خطأ يحدث أثناء تشغيل البرنامج.

مثال:

Divide by zero
Invalid memory access

⸻

 Standard Streams 📥📤

البرنامج يتعامل مع البيانات من خلال ثلاثة Streams أساسية:

Stream	الوظيفة
stdin	Standard Input
stdout	Standard Output
stderr	Standard Error

بشكل افتراضي:

Keyboard → stdin → Program → stdout → Screen
                         ↘️
                          stderr → Screen

لكن يمكن عمل Redirection للـ Streams بحيث تأتي البيانات من File بدل الـ Keyboard أو يتم حفظ الـ Output في File.


⸻

 Internet 🌐

من أهم اللبنات التاريخية للإنترنت:

ARPA → ARPANET

تم إنشاء ARPANET في أواخر الستينيات لربط أجهزة الكمبيوتر في المؤسسات البحثية والجامعات.

⸻

 TCP

TCP — Transmission Control Protocol

يساعد على توصيل البيانات بصورة موثوقة.

يمكن تخيل البيانات الكبيرة كأنها يتم تقسيمها إلى:

Packets

ثم يتم التعامل معها بحيث يمكن إعادة تجميع البيانات عند الوصول.

⸻

 IP

IP — Internet Protocol

يهتم بالعنونة والتعامل مع عناوين الأجهزة على الشبكة.

كل جهاز يمكن أن يكون له:

IP Address

بشكل مبسط:

TCP → Reliable Delivery
IP  → Addressing / Routing

⸻

 Internet vs Web

Internet

البنية التحتية التي تربط الأجهزة:

* Routers
* Cables
* Networks
* Servers

World Wide Web

خدمة تعمل فوق الإنترنت وتضم صفحات ومواقع الويب.

إذن:

Internet ≠ Web

⸻

 World Wide Web 🌍

ارتبط ظهور الـ Web بـ:

Tim Berners-Lee

في CERN سنة:

1989

ومن أهم التقنيات المرتبطة بالويب:

HTML

HyperText Markup Language

تستخدم لبناء صفحات الويب والروابط.

HTTP

HyperText Transfer Protocol

يستخدم لنقل موارد وبيانات الويب.

W3C

منظمة تهتم بوضع معايير للويب.

⸻

 IoT — Internet of Things 📡

الـ IoT يعني ربط الأشياء والأجهزة بالشبكة.

أمثلة:

* Sensors
* Smart Meters
* Temperature Sensors
* Medical Devices
* Tracking Devices

الفكرة:

Thing
 ↓
Network
 ↓
Data
 ↓
Software

⸻

 Cloud Computing ☁️

Cloud Computing يعني استخدام موارد حوسبية عبر الإنترنت بدل الاعتماد فقط على الجهاز المحلي.

يمكن أن تشمل:

* Computing Power
* Storage
* Databases
* Networking
* Software

ومن فوائدها:

* استخدام الموارد حسب الحاجة.
* تقليل الحاجة لشراء Hardware قوي.
* الاستفادة من خدمات جاهزة.
* إدارة وتحديث الموارد بواسطة مزود الخدمة.

⸻

 As a Service

أشهر النماذج:

SaaS

Software as a Service

استخدام Software كخدمة.

PaaS

Platform as a Service

استخدام Platform جاهزة لتطوير وتشغيل التطبيقات.

IaaS

Infrastructure as a Service

استخدام Infrastructure مثل:

* Servers
* Storage
* Networking

⸻

 Mashups 🧩

الـ Mashup هو دمج أكثر من Web Service لبناء تطبيق جديد.

مثال:

Real Estate Data
       +
Maps Service
       ↓
Real Estate Map Application

الفكرة:

Reuse existing services instead of building everything from scratch.

⸻

 Software Technologies 🛠️

Refactoring

تعديل وتنظيم الكود بدون تغيير وظيفته الأساسية.

Messy Code
    ↓
Refactoring
    ↓
Clean + Organized Code

أهدافه:

* Readability
* Maintainability
* Better Organization
* Easier Modification

⸻

Design Patterns

حلول وتصميمات مجربة لمشاكل برمجية متكررة.

Repeated Problem
       ↓
Known Pattern
       ↓
Reusable Solution

⸻

SDK

SDK — Software Development Kit

مجموعة أدوات وDocumentation تساعد المبرمج على بناء تطبيقات لمنصة معينة.

يمكن أن تحتوي على:

* Development Tools
* Libraries
* Documentation
* APIs
* Utilities

مثال:

iOS SDK

⸻

 Big Data 📊

Big Data تعني التعامل مع كميات ضخمة ومعقدة من البيانات.

أهم خصائصها:

Volume
Velocity
Variety
Veracity

⸻

 The Four Vs of Big Data

1️⃣ Volume

كمية البيانات.

How much data?

⸻

2️⃣ Velocity

سرعة توليد البيانات وحركتها وتغيرها.

How fast?

⸻

3️⃣ Variety

تنوع أنواع البيانات.

مثل:

Text
Images
Video
Audio
Sensor Data

How many types?

⸻

4️⃣ Veracity

مدى صحة وموثوقية البيانات.

Can we trust the data?

⸻

 Big Data Example — Social Media

تخيلي منصة Social Media:

Volume

مليارات المنشورات.

Velocity

البيانات والتفاعلات تحدث باستمرار.

Variety

Text
Images
Videos
Audio

Veracity

هل المعلومات المنشورة صحيحة أم Fake News؟

⸻

 Data Analysis

ظهر مصطلح Data Analysis في الستينيات.

ومع زيادة حجم البيانات وتطور قدرة الكمبيوتر على تخزينها ومعالجتها، أصبح تحليل البيانات مجالًا مهمًا جدًا.

⸻

 Moore’s Law

يرتبط Moore’s Law بالملاحظة التاريخية لتطور عدد الـ Transistors في الدوائر المتكاملة.

الفكرة العامة:

More Transistors
        ↓
More Computing Capability
        ↓
Lower Cost per Computing Capability

وساعد هذا التطور على:

* زيادة القدرة الحسابية.
* زيادة سعة التخزين.
* تقليل تكلفة معالجة البيانات.

⸻

 Goal of Computing 🧠

الفكرة المهمة:

The goal of computing is insight, not numbers.

أي أن الهدف من الحوسبة ليس مجرد إجراء الحسابات، وإنما الوصول إلى:

Data
 ↓
Analysis
 ↓
Understanding
 ↓
Insight

⸻

 Data Science Applications

علم البيانات يستخدم في مجالات كثيرة.

Healthcare 🏥

* Cancer Diagnosis
* Brain Mapping
* Electronic Health Records
* Medical Device Monitoring

Security 🔐

* Fraud Detection
* Cybersecurity
* Threat Detection

AI / NLP 🤖

* Machine Translation
* Text Summarization
* Emotion Detection
* Sentiment Analysis

Smart Cities 🏙️

* Autonomous Vehicles
* Smart Traffic
* Smart Homes
* Ride-sharing

⸻

 Big Data and AI

الـ Big Data ساعدت في تطور:

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Natural Language Processing

لأن كثيرًا من أنظمة التعلم تحتاج إلى كميات كبيرة من البيانات.

⸻

 Big Data and NLP

أمثلة:

CV Analysis
Text Summarization
Sentiment Analysis
Translation

البيانات هنا قد تكون:

Unstructured Text

ويتم استخدام تقنيات NLP لاستخراج المعلومات والمعنى منها.

⸻

 Veracity and AI Decisions ⚠️

جودة البيانات مهمة جدًا.

إذا كانت البيانات:

* Incorrect
* Incomplete
* Biased

فقد يتعلم النظام نتائج سيئة.

Bad Data
   ↓
Bad Model
   ↓
Bad Decisions

⸻

 Memory Limits 💾

في Problem Solving قد نجد:

Memory Limit: 256 MB

يجب أن نحسب كمية الذاكرة التي تحتاجها الـ Data Structures.

مثال:

100,000,000 integers

إذا كان:

int = 4 bytes

إذن:

100,000,000 × 4
=
400,000,000 bytes
≈ 400 MB

وهذا أكبر من:

256 MB

لذلك قد نحصل على:

Memory Limit Exceeded

⸻

 Data Size Units

الترتيب:

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

تقريبًا في النظام الثنائي:

1 MB ≈ 2²⁰ bytes
1 GB ≈ 2³⁰ bytes
1 TB ≈ 2⁴⁰ bytes

وفي النظام العشري:

1 PB = 1000 TB
1 EB = 1000 PB
1 ZB = 1000 EB

⸻

 Computing Power ⚡

تقاس القدرة على تنفيذ Floating-Point Operations باستخدام:

FLOPS

أي:

Floating-Point Operations Per Second

ومن الوحدات:

GFLOPS
TFLOPS
PFLOPS
EFLOPS

⸻

 Supercomputing

القدرات الحسابية الضخمة تستخدم في:

* Big Data
* Scientific Computing
* AI
* Simulations

ومن التقنيات المستخدمة:

* Powerful CPUs / GPUs
* Parallel Computing
* Distributed Computing
* Supercomputers

⸻

Quantum Computers ⚛️

Quantum Computing مجال مختلف عن الحوسبة التقليدية.

يستخدم:

Qubits

بدل الاعتماد فقط على Classical Bits.

وله تطبيقات محتملة في بعض أنواع المسائل، كما قد يؤثر مستقبلًا على بعض أنظمة التشفير.

⸻

 Energy Consumption 🔋

تشغيل أنظمة حوسبية قوية ومعالجة Big Data يحتاج إلى كميات كبيرة من الطاقة.

More Computing
      ↓
More Energy Demand

لذلك تصبح كفاءة الـ Hardware والـ Algorithms مهمة جدًا.

⸻

 Artificial Intelligence 🤖

AI — Artificial Intelligence

يهدف إلى بناء أنظمة تستطيع أداء مهام تتطلب عادةً قدرات ذكية.

أمثلة:

* Understanding Language
* Recognizing Patterns
* Playing Games
* Making Predictions
* Learning from Data

⸻

AGI

AGI — Artificial General Intelligence

هو مفهوم لنظام ذكاء اصطناعي عام يستطيع أداء مجموعة واسعة من المهام الذكية بطريقة عامة تشبه قدرات الإنسان.

⸻

 AI Timeline 🕐

1997 — Deep Blue

IBM’s Deep Blue هزم بطل العالم في الشطرنج.

اعتمد بدرجة كبيرة على:

* Search
* Massive Computation
* Hardware مخصص وقوي

⸻

2011 — Watson

IBM’s Watson فاز على متسابقين بارزين في:

Jeopardy!

واستخدم تقنيات مرتبطة بـ:

Natural Language Processing

لتحليل كميات ضخمة من المعلومات والإجابة عن الأسئلة.

⸻

2015 — AlphaGo

طورت Google DeepMind:

AlphaGo

للعب:

Go

واستخدم:

* Deep Learning
* Neural Networks

ونجح في هزيمة لاعب محترف في Go.

⸻

AlphaZero

AlphaZero استخدم:

Reinforcement Learning

وتعلم من خلال اللعب ضد نفسه.

الفكرة:

Rules
 ↓
Self-Play
 ↓
Learning
 ↓
Improvement

⸻

 Evolution of AI

يمكن تلخيص التطور:

Deep Blue
   ↓
Search + Massive Computation
   ↓
Watson
   ↓
Language + Information Processing
   ↓
AlphaGo
   ↓
Deep Learning
   ↓
AlphaZero
   ↓
Self-Play + Reinforcement Learning

⸻

 The AI Effect

هناك فكرة معروفة:

Once a problem is solved successfully, people may stop considering it “AI” and see it as ordinary software.

أي أن بعض المهام التي كانت تعتبر AI تصبح مع الوقت جزءًا من البرمجيات العادية.

⸻

38. Hardware + Software

من أهم أفكار الشابتر:

Software
+
Algorithms
+
Hardware
=
Computing System

الأداء لا يعتمد على الـ Software فقط.

فالـ Hardware Architecture يمكن أن يجعل خوارزمية معينة عملية في وقت معين.

⸻

🧠 Final Big Picture



Programming Languages
          ↓
       Source Code
          ↓
Edit → Preprocess → Compile → Link
          ↓
         Load
          ↓
       Execute
          ↓
       Computer
          ↓
      Networking
          ↓
       Internet
          ↓
         Web
          ↓
        Cloud
          ↓
       Big Data
          ↓
     Data Science
          ↓
Artificial Intelligence
          ↓
 Machine Learning
          ↓
   Deep Learning
          ↓
       Insight

⸻

🎯 أهم الحاجات اللي لازم أفتكرها

Programming Languages

C/C++     → Performance + Hardware
Python    → AI + Data Science
Java      → JVM + Enterprise
JavaScript→ Web + Node.js
C#        → Microsoft + Applications
Swift     → Apple
R         → Statistics + Data Analysis

Program Execution

Edit
→ Preprocess
→ Compile
→ Link
→ Load
→ Execute

Internet

TCP → Reliable Delivery
IP  → Addressing / Routing

Web

HTML → Structure
HTTP → Communication
WWW  → Web

Cloud

SaaS
PaaS
IaaS

Big Data

Volume
Velocity
Variety
Veracity

Software Engineering

Refactoring
Design Patterns
SDKs

AI

Deep Blue
   ↓
Watson
   ↓
AlphaGo
   ↓
AlphaZero

⸻

🏁 Chapter 1 — Final Takeaway

Computer Science مش مجرد كتابة كود.

إحنا بنبدأ من:

Programming

ثم نفهم:

How Code Is Compiled
How Programs Run
How Computers Communicate
How the Internet Works
How the Web Works
How Cloud Systems Work
How Massive Data Is Stored and Processed
How Data Science Extracts Insights
How AI Learns From Data

وفي النهاية:

Code
 ↓
Computer
 ↓
Network
 ↓
Cloud
 ↓
Big Data
 ↓
Data Science
 ↓
AI
 ↓
Insight

🎉 End of Chapter 1

