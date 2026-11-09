# Generic Tasks

## Task 1: Print It Yourself

**Design a Simple Part and 3D Print It**

First learn how a 3D printer works. Then design your own simple parts, a cube and a cylinder, in Onshape. It runs in your browser, so there is nothing to install. No CAD experience needed, so students from any branch can do it. After that, slice your design and print it.

**Objective:** Know the full process of 3D printing: design, STL file, slicing and printing.

### What to do

1. Watch the intro video on 3D printers and read the PLA settings guide.
2. Go through the 3D printer SOPs.
3. Make an Onshape account with your college email.
4. Read the Onshape article below. Design a cube (30 mm sides) and a cylinder (30 mm diameter, 30 mm height) as two separate parts.
5. Export them as an STL file in millimeters.
6. Slice the STL in Bambu Lab studio. Note down the bed temperature and infill density.
7. Print it with a coordinator present.

### Learning Resources

- [Introduction to 3D Printer](https://www.youtube.com/watch?v=kM5zRO3n9-Y): how a 3D printer works.
- [PLA Printing Guide](https://standardprintco.com/read/pla-filament-printing-guide-how-to-succeed-printing-pla-and-troubleshooting-common-problems-step-by-step): bed temperature, infill and other PLA settings.
- [Types of 3D Printing](https://formlabs.com/asia/blog/fdm-vs-sla-vs-sls-how-to-choose-the-right-3d-printing-technology/): FDM vs SLA vs SLS.
- [Designing a Simple Part in Onshape for 3D Printing](https://github.com/prajwaldhannur4-code/3d-design-onshape-guide/blob/main/README.md): Refer the Resource Article.

### Suggested Focus

Read the Onshape article first, then start designing. Type mm after every number. Keep the cube and cylinder as separate parts. Check that the STL is in millimeters before slicing.

**Note:** Printing is done only with a coordinator presence.

---

## Task 2: Dynamic Portfolio & Admin Dashboard

### Task Description

Design and develop a dynamic personal portfolio website along with an administrative dashboard that allows the portfolio owner to manage website content through a graphical interface without modifying the source code.

The application should consist of two integrated interfaces:

1. A public portfolio website that showcases the student's profile, skills, projects, and achievements.
2. An admin dashboard that allows the owner to manage and update portfolio content dynamically.

### Requirements

#### 1. Public Portfolio
- Develop a responsive website displaying the student's profile, skills, projects, and achievements.
- Retrieve and display portfolio content dynamically through an API.
- Ensure that changes made through the admin dashboard are reflected on the public portfolio.

#### 2. Admin Dashboard
- Create a user-friendly administrative interface for managing portfolio content.
- Implement functionality to add, view, update, and delete projects and skills using forms and controls.
- Ensure that content management does not require direct modification of the source code.

#### 3. REST API Development
- Develop and integrate a RESTful API to facilitate communication between the admin dashboard, backend, and public portfolio.
- Implement appropriate API endpoints and HTTP methods for creating, retrieving, updating, and deleting portfolio content.
- Exchange data using JSON and implement basic input validation and error handling.

#### 4. Data Management
- Store and manage portfolio content using an appropriate in-memory data structure or another beginner-friendly mechanism.
- Ensure that both the public portfolio and admin dashboard access the same application data.
- Database integration is not required.

#### 5. Deployment and Documentation
- Deploy the application using suitable hosting platforms.
- Maintain the source code in a GitHub repository.
- Document the application architecture, API endpoints, setup instructions, and known limitations in a README file.

### Expected Outcomes
- Understand the development of dynamic and responsive web applications.
- Learn the fundamentals of REST APIs, HTTP methods, and JSON.
- Understand CRUD operations and client-server communication.
- Gain experience integrating frontend interfaces with an API.
- Develop skills in application deployment, documentation, and error handling.

### Suggested Technologies
HTML, CSS, JavaScript, and any suitable backend technology or framework of the student's choice.

### Submission Requirements
1. Public portfolio website URL.
2. Admin dashboard URL or route.
3. GitHub repository link.
4. README documentation.
5. Screenshots demonstrating content management and dynamic updates.

### Resources
1. [MDN: Getting Started with Web Development](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started)
2. [Postman: Getting Started Quick Start](https://learning.postman.com/docs/getting-started/quick-start/)
3. [MDN: Network Requests](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Network_requests)

---

## Task 3: Working with GitHub

Familiarize yourself with real-world Git and GitHub workflows including Issues, Branching, Resolving Merge Conflicts, Pull Requests, and GitHub Actions (CI/CD).

Given below is the task repository. Follow the instructions in its `README.md` to generate your username-specific assignment, document the bugs you find in a GitHub Issue, fix them on a new branch, resolve the practice merge conflict, and open a Pull Request.

### What to include in your task report:
1. The output of `python my_task.py <your-github-username>` showing your assigned functions.
2. A link to the GitHub Issue you opened and a brief explanation of the bugs you fixed.
3. A link to your Pull Request showing the passing GitHub Actions check (Note: PRs are verified by CI and left open for review they do not need to be merged).

**Check this link for more info:** [https://github.com/UVCE-Marvel/git-task](https://github.com/UVCE-Marvel/git-task)

---

## Task 4: Hack the hardware

### Objective: Ubuntu Command Line: Systems Computing, Architecture & Linux

### Core Intention
To move beyond rote command memorization and cultivate a deep, foundational understanding of computing systems, the Linux operating system, and system-level problem-solving. Students learn *how* and *why* their terminal commands navigate the software stack—from high-level shell calls down to execution units in hardware.

### 1. Hardware Foundation & Architecture: "The 'U' in CPU"

#### Topics & Concepts
- **The Anatomy of the CPU:** The Control Unit (CU), Arithmetic Logic Unit (ALU), internal registers (A, D, Program Counter PC), and bus connections.
- **The Fetch-Decode-Execute Cycle:** How machine instructions are fetched from memory, decoded by control logic, executed inside the ALU, and written back to registers/RAM.
- **Hardware Abstraction:** How shell instructions translate through compiler/assembler pipelines into binary micro-operations that flip physical logic gates.

#### Why You Need This
Understanding hardware abstraction stops you from treating the terminal as a black box. Knowing how registers, memory addresses, and execution cycles work allows you to diagnose performance bottlenecks, manage low-level system resources, write efficient code, and program embedded microcontrollers or microprocessors effectively.

#### How to Study This Topic
1. **Nand2Tetris Unit 4 (Machine Language):** Write assembly programs for the Hack computer (Mult.asm and Fill.asm) to manually track register states (A, D, M), instruction decoding, and memory-mapped I/O (Screen and Keyboard).
2. **Trace Hardware Metrics via Terminal:** Use terminal utilities like `lscpu`, `lsscsi`, and `cat /proc/cpuinfo` to map abstract CPU concepts (cores, threads, cache sizes, architecture flags) to physical host hardware.

### 2. Operating Systems, Kernels, and Linux Distributions

#### Topics & Concepts
- **The Operating System's Core Role:** Memory virtualization, process scheduling, storage management, and hardware safety.
- **What is a Kernel?** The privileged (Ring 0) bridge between user space applications and physical hardware via System Calls (syscalls).
- **Linux Distributions vs. The Kernel:** Distinguishing between the upstream Linux kernel and distributions (Ubuntu, Debian, Fedora, Arch) that package userland tools, package managers, and display servers.

#### Why You Need This
When a application or script crashes, hangs, or fails to start, the issue usually lies in kernel-level resource access, missing dependencies, or system call errors. Understanding OS mechanics enables you to debug real-world server, embedded Linux, and edge-computing environments.

#### How to Study This Topic
1. **System Call Observation:** Run simple terminal commands through `strace` (e.g., `strace ls`) to observe how userland utilities request kernel services (e.g., `openat`, `read`, `write`).
2. **Virtual Filesystem Exploration:** Navigate `/proc` and `/sys` to understand how the Linux kernel exposes running system states directly as text files.

### 3. The Linux Environment & Core System Concepts

#### Topics & Concepts
- **Terminal vs. Shell:** Distinguishing between terminal emulators (user interface) and shells (bash, zsh — command interpreters).
- **Filesystem Hierarchy Standard (FHS):** Root (/), user space (~), device files (/dev), configuration files (/etc), and system binaries (/bin, /usr/bin).
- **Permissions & Security Model:** Read, write, execute (rwx) flags, file ownership (user:group), and privilege escalation (sudo).
- **Processes & Signals:** Process IDs (PIDs), job control (&, fg, bg), environment variables, standard streams (stdin, stdout, stderr), and piping (|).

#### Why You Need This
The command line is the primary interface for remote servers, cloud infrastructure, robotics platforms (like ROS 2), and build environments. Mastering streams, permissions, and process controls lets you automate complex workflows and manage systems without relying on a graphical user interface.

#### How to Study This Topic
1. **Interactive Terminal Scenarios:** Solve practical system issues (e.g., permission-denied errors, locating run-away processes with `top` or `ps aux`, killing stuck tasks via signals).
2. **Pipe Construction:** Practice stringing fundamental tools (`grep`, `awk`, `sed`, `cut`, `sort`) together to parse logs and extract target metrics.

### 4. Practical Tips for Terminal Execution
- **Read the Manual (man):** Never guess command flags. Run `man <command>` (or use `tldr <command>`) to inspect flags and syntax.
- **Inspect Exit Codes:** Check `$?` immediately after running a command to see if it succeeded (0) or threw an error (non-zero).
- **Fail Fast & Safely:** Use `ls` or `echo` to verify wildcard patterns (e.g., `echo *.log`) before executing destructive commands like `rm *.log`.
- **Understand Standard Streams:** Treat stdout (1) and stderr (2) separately so you don't miss error messages when redirecting logs.
- **Leverage Autocompletion & History:** Use Tab key completion to avoid typos and Ctrl + R to search previous command history quickly.

### 5. Hands-on Problem Statement: System Audit & Log Processing Pipeline

You are tasked with inspecting a remote Linux workstation that has experienced intermittent slowdowns. Without using any Graphical User Interface (GUI), complete the following steps using terminal utilities:

1. **Hardware & Kernel Inspection:** Identify the total number of physical CPU cores, architecture model, and the running Linux kernel version. Output these values into a file named `system_summary.txt`.
2. **Process & Resource Triage:** Locate all running processes consuming memory on the system. Filter out system daemons to find the process ID (PID) of the process running under your user space, and write the output to `process_audit.log`.
3. **Permission & File System Reorganization:**
   - Create a secure directory structure under `~/workspace/audit_logs/`.
   - Change the directory permissions so that only your user has read, write, and execute permissions (700). Move all generated log files into this directory.
4. **Log Data Parsing & Filtering:** Given a system log file containing mixed informational and error entries, write a single-line command pipeline using `cat`, `grep`, `awk`, and `sort` to extract only unique [ERROR] messages and count their occurrences.

### 6. What You Must Build

To successfully complete this task, you must build and deliver:

1. **Draw ur own Architecture:** So draw how u think the CPU used to look before going through it and how it looks now according to u. Wrong answers welcomed but want to see ur understanding.
2. **Custom Automated Shell Script (system_health.sh):** A bash script that gathers system uptime, CPU core count, active memory usage from `/proc/meminfo`, and active user processes, formatting them into a readable text report.
3. **Execution & Analysis Log Notebook:** A written document explaining:
   - The step-by-step resolution of the **Problem Statement**.
   - Annotations of key strace outputs showing at least two system calls (`openat`, `write`).
   - Explanations for why specific piping choices (|) were used during log extraction.

### 7. Foundational Command-Line Exercises
- **Navigation & Inspection:** `pwd`, `cd`, `ls -la`, `tree`
- **File & Directory Operations:** `touch`, `mkdir -p`, `cp -r`, `mv`, `rm -rf`
- **Content Viewing & Inspection:** `cat`, `less`, `head`, `tail -f`, `echo`, `grep`

### 8. Resource Links

#### Computer Architecture & Nand2Tetris
- [**Nand2Tetris Official Course & Software Suite**](https://www.nand2tetris.org/software): Hands-on building of a computer system from basic NAND logic gates up to an Operating System.
- [**Nand2Tetris Unit 4 (Machine Language)**](https://www.nand2tetris.org/project04): Covers Hack assembly programming, register operations (A, D, M), pointer manipulation, and memory-mapped I/O.
- [**Nand2Tetris Chapter 5 (Computer Architecture)**](https://www.nand2tetris.org/): Focuses on building the Hack CPU, instruction decoding logic, and memory integration.

#### Linux & Command Line Fundamentals
- [**The Linux Command Line by William Shotts (Free PDF)**](https://linuxcommand.org/tlcl.php): Comprehensive reference covering basic shell operations, environment management, and shell scripting.
- [**Linux Journey**](https://linuxjourney.com/): Interactive, modular guide breaking down Linux command line operations, text manipulation, permissions, process handling, and kernel mechanics.
- [**LinuxCommand.org Tutorials**](https://linuxcommand.org/): Structured, step-by-step tutorials on command execution, storage navigation, and terminal problem-solving.
- [**TLDR Pages**](https://tldr.sh/): Community-driven, simplified man pages focusing on practical, real-world command usage examples.

---

## Task 5: Operation Blackout

### Decode the Hidden Message

An unknown source has transmitted a mysterious sequence of numbers, and your mission is to uncover the secret hidden within it. The data may appear random, but with the right transformations, a meaningful pattern will emerge.

Using NumPy, investigate the encoded array, reshape it into a square matrix, experiment with transposing and reversing its elements, and visualize the result using Matplotlib. Follow the cryptic clues, piece together the original arrangement, and reveal the hidden message!

Can you crack the code and complete Operation Blackout?

**Download the Numpy Array:** [https://drive.google.com/file/d/1lbzxfFuLJSNRXZqT63z8teFWCT44xfRk/view?usp=drivesdk](https://drive.google.com/file/d/1lbzxfFuLJSNRXZqT63z8teFWCT44xfRk/view?usp=drivesdk)

### Learning Resources

#### NumPy
- [NumPy Quickstart — Official Documentation](https://numpy.org/doc/stable/user/quickstart.html) — Array shapes, indexing, slicing, and transformations.
- [Indexing on ndarrays — NumPy](https://numpy.org/doc/stable/user/basics.indexing.html) — Array indexing and slicing.
- [NumPy Tutorial — W3Schools](https://www.w3schools.com/python/numpy/default.asp) — Beginner-friendly reference.
- [NumPy Tutorial — DataCamp](https://www.datacamp.com/tutorial/python-numpy-tutorial) — Tutorial covering common NumPy operations.

#### Matplotlib
- [Matplotlib Tutorials — Official Documentation](https://matplotlib.org/stable/tutorials/index.html) — Plotting fundamentals and customization.
- [imshow() — Matplotlib Documentation](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.imshow.html) — Display a 2D array as an image.
- [Colormap Guide — Matplotlib](https://matplotlib.org/stable/users/explain/colors/colormaps.html) — Choose a colormap for visualizing the matrix.
- [Matplotlib Tutorial — DataCamp](https://www.datacamp.com/tutorial/matplotlib-tutorial-python) — Introduction to plotting with Matplotlib.

### YouTube Videos
- [NumPy Tutorial for Beginners — Keith Galli](https://www.youtube.com/watch?v=QUT1VHiLmmI) — Arrays, slicing, reshaping, and other NumPy basics.
- [NumPy Tutorial — Corey Schafer](https://www.youtube.com/watch?v=GB9ByFAIAH4) — A second explanation of NumPy fundamentals.
- [Matplotlib Tutorial — freeCodeCamp](https://www.youtube.com/watch?v=3Xc3CA655Y4) — Creating and customizing plots.
- [Introduction to Numerical Computing with NumPy — Enthought](https://www.youtube.com/results?search_query=Introduction+to+Numerical+Computing+with+NumPy+Alex+Chabot-Leclerc) — Search link for a practical NumPy workshop.

### Suggested Focus
Before solving the puzzle, review array size and shape, reshape(), transpose(), slicing, and reversing with negative-step slices. Then review imshow() and colormaps. Check that the number of array elements matches the target matrix dimensions before reshaping.

**Note:** The resources are supplementary learning materials. Students should understand and explain the transformations and model operations used in their own solutions.

---

## Task 6: Build Your Own Brain

### Linear Regression from Scratch

In this task, you will implement a Linear Regression model from scratch using NumPy to develop a deeper understanding of the underlying principles of machine learning. Using the California Housing dataset, you will train your model using Gradient Descent, investigate the effects of learning rate and feature scaling, and visualize the model’s learning process.

You will then compare your implementation with `sklearn.linear_model.LinearRegression` using standard evaluation metrics, including MSE, MAE, and R². Through this comparative analysis, you will gain practical insights into model optimization, performance evaluation, and the advantages of established machine learning libraries.

**Objective:** Develop a fundamental understanding of Linear Regression by implementing, evaluating, and comparing a custom model against a standard library implementation.

### Learning Resources

#### Concepts and implementation
- [Google Machine Learning Crash Course: Linear Regression](https://developers.google.com/machine-learning/crash-course/linear-regression) — Introduction to linear regression, features, predictions, and loss.
- [Google Machine Learning Crash Course: Gradient Descent](https://developers.google.com/machine-learning/crash-course/linear-regression/gradient-descent) — How gradient descent updates model parameters.
- [California Housing Dataset — scikit-learn](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset) — Dataset description and loading information.
- [StandardScaler — scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) — Feature standardization.
- [LinearRegression — scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html) — Reference for the library implementation.
- [Regression Metrics — scikit-learn](https://scikit-learn.org/stable/modules/model_evaluation.html) — Evaluation metrics and model assessment.
- [Coding Linear Regression from Scratch — Towards Data Science](https://towardsdatascience.com/coding-linear-regression-from-scratch-c42ec079902) — Supplementary implementation walkthrough.
- [Linear Regression from Scratch — AskPython](https://www.askpython.com/python/examples/linear-regression-from-scratch) — Step-by-step coding reference.

### YouTube Videos
- [Linear Regression, Clearly Explained — StatQuest](https://www.youtube.com/watch?v=7ArmBVF2dCs) — Understand the intuition behind fitting a line and R².
- [Gradient Descent, Step-by-Step — StatQuest](https://www.youtube.com/watch?v=sDv4f4s2SB8) — Visual explanation of gradient descent and parameter updates.
- [Linear Regression from Scratch with NumPy — MLTut](https://www.youtube.com/watch?v=DYM40H8ydnc) — Code a basic regression model with NumPy, MSE, and gradient descent.
- [Building the Gradient Descent Algorithm — Nicholas Renotte](https://www.youtube.com/results?search_query=Building+the+Gradient+Descent+Algorithm+Nicholas+Renotte) — Search link for a practical coding walkthrough.

### Suggested Focus
Start with the linear regression and gradient descent videos before coding. Then implement the model using NumPy, standardize features using training data only, and compare both models on the same held-out test set. Plot the loss over iterations and compare MSE, MAE, and R².

---

## Task 7: Resource Article writing using Markdown

Markdown is an easy-to-use markup language that is used with plain text to add formatting elements (headings, bulleted lists, URLs) to plain text without the use of a formal text editor or the use of HTML tags. Markdown is device agnostic and displays the writing format consistently across device type. Write a technical resource article on a topic of your choice and post it on the MARVEL website. Refer to the linked article for further details.

**LINK:** [https://hub.uvcemarvel.in/article/52f92f36-fb8a-45da-8f28-686bf4efefff](https://hub.uvcemarvel.in/article/52f92f36-fb8a-45da-8f28-686bf4efefff)

---

## Task 8: Arduino vs ESP32

**NOTE -** Before working on this task it is mandatory to have read the basics of Arduino Uno and ESP32 task. Without finishing that do not work on this task.

### Arduino UNO vs ESP32: Sensor-Based DC Motor Control

#### Problem Statement
Build a DC motor control system using Arduino UNO R3 and ESP32 to compare their pin configurations, analog inputs, PWM control, and voltage levels. Use an HC-SR04 ultrasonic sensor to measure distance and a potentiometer to control motor speed through a suitable motor driver. The motor must stop when an object comes closer than a predefined distance of 15 cm. Implement the same basic setup on both boards, ensuring that all sensor signals are compatible with the selected board. Finally, extend the ESP32 setup with a web page that allows users to control motor speed using a slider and stop the motor using a button. Identify what additional hardware the Arduino UNO would need to support similar Wi-Fi control.

**Tips -** Before working on hardware make a simulation for better understanding:
1. For arduino uno use **Tinkercad** a beginner friendly web based software for electronics.
2. For ESP32 use **Wokwi** simulation another web based software for electronics.

#### Why You’ll Need This
Arduino UNO and ESP32 can perform similar tasks, but their pin configurations, voltage levels, analog inputs, PWM capabilities, and wireless features differ. A circuit that works on one board may need changes before it can work safely on the other.

Through this task, you will explore these differences by building and testing the same application on both boards. You will also learn why a sensor powered by 5 V may require voltage conversion before its output can be connected to the ESP32's 3.3 V GPIO, and how PWM can be used to control motor speed.

#### What You Must Build
1. **Sensor and motor control:** Connect the HC-SR04, potentiometer, and DC motor through a suitable motor driver. Use the potentiometer to vary motor speed and display distance readings on the Serial Monitor. The motor must stop when an object is detected within 15 cm.
2. **Implement on both boards:** Build and test the same basic system using Arduino UNO R3 and ESP32. Identify the required pins and adapt the wiring and code for each board.
3. **Check voltage compatibility:** Determine the voltage requirements of each component. Use suitable voltage-conversion circuitry for the HC-SR04 Echo signal when connecting it to the ESP32, and ensure the potentiometer output stays within the board's permitted input voltage.
4. **Add web-based control:** Extend the ESP32 program with a web page containing a speed slider from 0% to 100% and a Stop button. The web interface must control motor speed, while the distance-based stop condition must override the selected speed.
5. **Compare the boards:** Document the differences you observed in pin usage, analog readings, PWM implementation, voltage compatibility, and Wi-Fi setup. Explain what additional compatible hardware would be required to provide similar web-based control using Arduino UNO R3.

#### Learn Before You Build
1. [**Arduino — PWM Output Guide**](https://support.arduino.cc/hc/en-us/articles/9350537961500-Use-PWM-output-with-Arduino) and [**ESP32 — PWM Documentation**](https://docs.espressif.com/projects/arduino-esp32/en/latest/api/ledc.html) to understand and compare PWM control.
2. [**Voltage Divider Tutorial**](https://learn.sparkfun.com/tutorials/voltage-dividers) to learn how to reduce a sensor's output voltage safely.

**For web servers:-**
1. [https://randomnerdtutorials.com/esp32-web-server-slider-pwm](https://randomnerdtutorials.com/esp32-web-server-slider-pwm)
OR
2. [https://randomnerdtutorials.com/esp32-web-server-dc-motor-arduino](https://randomnerdtutorials.com/esp32-web-server-dc-motor-arduino)

Work through these resources before starting the implementation. Test the basic circuit on both boards first, then add web-based control to the ESP32. Record your observations and explain the differences you discover.

---

## Task 9: The “Joint” Venture - Soldering

### What are you required to do ?

1. Go around the soldering station, look at all the equipment and try to figure out what they do and what they are.
2. Gather your domain batchmates and get a one-time briefing from any of your domain coordinators on this task.
3. Solder a simple circuit (Led Fader Circuit) on a perf-board. To be done Individually.
   - Video Guide: [UVCE MARVEL : Soldering on perfboard](https://www.youtube.com/watch?v=2coq-J3rIDQ)
   - Circuit link: [Tinkercad LED Fade Circuit](https://www.tinkercad.com/things/9rZOusbVsdD-led-fade-circuit?sharecode=qBo7A4CtXjYR5wEstvgI52fzG5-VooVDijic3irOY-Y)
   - Refer to the above link for circuit connections.
   - Oscilloscope is optional but using it would get you additional credit points.
   - Components you’ll be requiring = 1nos 100 micro farad capacitor, 1nos 1K resistor, 1nos 10k resistor, 1nos generic PN junction diode, 1nos LED of your choice, 1nos pushbutton (do not use any other kind of switches) and Power supply rated anywhere from 5V - 9V.
   - Check the working of the circuit.
   - Wiring should be done using single stranded wires.
   - Tinning is an advisory method while soldering wires, as it assures contacts are stable and not loose.
4. Theoretical knowledge buildup - Composition of Solder wire, flux.
5. Types of board - PCB, BreadBoard, ZeroPCB (Perfboard):
   - [MARVEL : Circuit on the breadboard](https://www.youtube.com/watch?v=gTYItNRoV-A)
   - [UVCE MARVEL : Soldering on perfboard](https://www.youtube.com/watch?v=2coq-J3rIDQ)
   - [Board Types Resource](https://youtu.be/w0c3t0fJhXU?si=HzJQMDstaUzv_fAE)
6. Hazards and Safety measures of Soldering. Resource : [https://youtu.be/AqvHogekDI4?si=GofaPrza3gG6vJOZ](https://youtu.be/AqvHogekDI4?si=GofaPrza3gG6vJOZ)

---

## Task 10: VRPS, OSCILLOSCOPE

Soon

---

## Task 11: 555 Astable Multivibrator with 60% Duty Cycle

### Objective

Design, build and measure a 555 astable multivibrator. By the end you should be able to:

* Choose the timing resistors and capacitor for a target frequency and duty cycle.
* Wire the NE555 as an astable oscillator on a breadboard.
* Measure frequency, high time and duty cycle on a digital storage oscilloscope (DSO).
* Explain any gap between the designed and the measured values.

### The Task

Design a 555 astable multivibrator whose output has a 60% duty cycle, build it on a breadboard, and observe the output on a DSO using the probes.

Pick a target frequency of 1 kHz so the waveform is easy to read on the scope (use another frequency only if your lab specifies one).

### Steps

1. **Read first.** Go through the resources below until you can write the astable formulas for frequency and duty cycle in terms of R₁, R₂ and C, and explain what charges and discharges the capacitor in each half of the cycle.
2. **Design on paper.** From the target frequency and 60% duty cycle, work out the ratio of R₁ to R₂, then choose C and compute the resistor values. Show every step.
3. **Pick real parts.** Round your resistors to standard values from the kit and recompute the frequency and duty cycle you will actually get.
4. **Build.** Wire the NE555 on the breadboard with a 5 V to 12 V supply, your R₁, R₂ and C, and a small capacitor (about 10 nF) from the control pin to ground. Check the datasheet pinout before powering up.
5. **Probe.** Connect the DSO probe to the output pin and ground. Set the timebase so that 2 to 3 full periods are visible, and make sure the probe is in the correct attenuation setting.
6. **Measure.** Record the period, frequency, high time and low time, and compute the duty cycle. Use the DSO’s cursors or automatic measurements, and note which one you used.
7. **Compare.** Put designed, calculated-with-real-parts and measured values side by side, and explain the differences (component tolerance, probe loading, scope accuracy).

### Deliverable

1. Design sheet (photo or scan is fine) with the equations, the ratio you derived, the chosen component values, and the recomputed frequency and duty cycle for the real parts.
2. Circuit schematic with all component values labeled.
3. Breadboard photo of the working circuit with the probe connected.
4. DSO screenshot or photo showing at least 2 periods of the output, with the measured frequency, high time and duty cycle visible.
5. Comparison table: designed vs. calculated (real parts) vs. measured, for frequency and duty cycle.
6. Short answer (3 to 4 sentences): why can a basic 555 astable (two resistors and one capacitor) never give a duty cycle below 50%, and why is 60% reachable without any extra parts?

### Resources

#### Reading
1. [555 Timer Math](https://www.mathscinotes.com/2014/04/555-timer-math/): derives the astable frequency and duty cycle, and the formulas for choosing R₁ and R₂ from a target frequency, duty cycle and C. The equations themselves are in images on the page.
2. [Astable Multivibrator using IC 555 (IIT Kharagpur virtual lab)](https://aec-iitkgp.vlabs.ac.in/exp/astable-multivibrator/pretest.html): lab-style pre-test on the same experiment.
3. [NE555 datasheet (Texas Instruments)](https://www.ti.com/lit/ds/symlink/ne555.pdf): pinout, supply range and the standard astable circuit.

#### Videos (YouTube)
1. [Astable 555 timer](https://youtu.be/kRlSFm519Bo): An amazing video by Ben Eater.
2. [555 Timer as Astable Multivibrator (Working, Design and Derivations)](https://www.youtube.com/watch?v=iJYm_BGqa1A): A second explanation of the same circuit.
3. [Measuring Frequency, Duty Cycle, & Pulse Width](https://www.youtube.com/watch?v=pty9YIdi9GU): How to read these off a scope.

#### Tools
A DSO with a 10x probe. Check the attenuation setting and compensate the probe on the scope’s calibration output before measuring.

Optional: simulate the circuit first in [Tinkercad Circuits](https://www.tinkercad.com/circuits) to check your component values before building.

---

## Task 12: Prime Number Detector with a K-Map

### Objective

Learn Karnaugh maps from scratch by using one to design a real circuit. By the end you should be able to:

* Fill a K-map from a truth table.
* Circle valid groups (sizes 1, 2, 4, 8) and read an equation off them.
* Explain why grouping works: two cells that touch differ in exactly one input, so that input drops out.
* Build the result in logic gates and check it against every input combination.

### The Task

Design and build a circuit with four inputs D C B A (a 4-bit number from 0 to 15, A is the least significant bit). The output LED turns on when the number is prime. Treat 0 and 1 as not prime.

Do this in Tinkercad Circuits using four slide switches as inputs, one LED as output, and plain gates (AND, OR, NOT) in between. No decoder or other “smart” ICs.

### Steps

1. Read first. Go through the K-map resources below until you can answer: what does it mean for two cells to “touch”, and what are the legal group sizes?
2. Truth table. Write all 16 rows and mark the output for each.
3. Raw circuit. Write one AND term for every row where the output is 1, OR them together, and build it in Tinkercad. Count the gates. This is your baseline.
4. K-map. Fill in the blank map below from your truth table (cell numbers are the decimal value of D C B A).
5. Group. Circle groups of 1s. Use the largest groups you can, let groups overlap, and remember that the edges of the map wrap around (left touches right, top touches bottom).
6. Equation. Write one product term per group and OR them.
7. Simplified circuit. Build it in Tinkercad and count the gates.
8. Verify. Run through all 16 switch combinations and confirm both circuits match your truth table. Write down your predicted output for 3 inputs before testing them.

#### Blank K-map (rows D C, columns B A)

```text
+----------+----+----+----+----+
| D C \ BA | 00 | 01 | 11 | 10 |
+----------+----+----+----+----+
|    00    |  0 |  1 |  3 |  2 |
|    01    |  4 |  5 |  7 |  6 |
|    11    | 12 | 13 | 15 | 14 |
|    10    |  8 |  9 | 11 | 10 |
+----------+----+----+----+----+
```

| D C \ B A | 00 | 01 | 11 | 10 |
| :---: | :---: | :---: | :---: | :---: |
| **00** | 0 | 1 | 3 | 2 |
| **01** | 4 | 5 | 7 | 6 |
| **11** | 12 | 13 | 15 | 14 |
| **10** | 8 | 9 | 11 | 10 |

*Axis order is 00, 01, 11, 10 on purpose, so that neighbouring cells always differ in only one input. Use it as given.*

### Deliverable

1. Tinkercad share link (viewable by anyone with the link) containing both the raw and the simplified circuit, labeled.
2. One sheet (photo or scan is fine) with the truth table, the filled K-map with groups circled, and your final equation.
3. Prediction table: 3 inputs, your predicted output, and the actual output.
4. Gate counts: raw circuit vs. simplified circuit.
5. Short answer (3 to 4 sentences): why can two touching cells be merged into one term?

### Resources

1. [Karnaugh map playlist](https://www.youtube.com/playlist?list=PLBlnK6fEyqRiLCE18N9RN8ymscpMaGCfk): the main K-map course. Cover the introduction and the 4-variable videos (grouping and wrap-around) before starting the task.
2. [Karnaugh Maps with 4 Variables](https://www.youtube.com/watch?v=YJSqf_Z024w): a second explanation of the same material, useful if the playlist doesn’t click.
3. [Logic Gates in Tinkercad](https://www.youtube.com/watch?v=ZIMcNXUzTkA): placing gates, switches and LEDs and running the simulation.
4. [Digital Electronics: Logic Gates Circuits on TinkerCad (playlist)](https://www.youtube.com/playlist?list=PLI3bPjdny_5F5Ma16wtAC81AtzwtDB7-8): more Tinkercad gate builds if you get stuck wiring.

#### Practice
[Karnaugh Mapping worksheet (All About Circuits)](https://www.allaboutcircuits.com/worksheets/karnaugh-mapping/): a few questions to try before you start the task.

#### Tools
[Tinkercad Circuits](https://www.tinkercad.com/circuits)

---

## TASK 13: Active Participation

Take part in any technical event, inter or intra college and submit the issued certificate of participation.

Enroll for a MOOC and complete the course.

---

## TASK 14: Datasheets report writing

Topics: 1) MQ135 Gas sensor 2) L293D motor driver

**Task Description:** Study the datasheet of any one of the above and write a report on it. Specify about the ICs used in L293D, PWM, H-bridge etc. In case of MQ 135, specify the calibrations for different gases and the Freundlich Absorption Theorem Graph.

---

## TASK 15: Sad servers - "Like LeetCode for Linux"

Sadservers is an excellent ground to test your Linux troubleshooting skills. Here is a troubleshooting scenario: Command Line Murders. Troubleshoot and Make Sad Servers Happy!

- [Command Line Murders Scenario](https://sadservers.com/scenario/command-line-murders)
- [Linux Commands Tutorial](https://www.hostinger.com/tutorials/linux-commands)
- [Learn Linux Commands Reference](https://github.com/vvvvvvss/learnLinux)
