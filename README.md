# 🏎️ Atomic Racers

<p align="center">
  <img width="500" height="500" alt="Atomic Racers Logo" src="https://github.com/user-attachments/assets/35946578-4e4f-47b9-a33e-2162b42a996f" />
</p>

**Project Role:** `ECS Programmer` | `Network Developer` | `3D Generalist`  
**Tech Stack:** `Custom C++ Engine` | `ECS Architecture` | `Utility AI`  
**Team Size:** 5 Members (9-month development cycle)

Atomic Racers is a high-speed arcade racing experience developed on a custom-built C++ engine. The project emphasizes fluid vehicle physics, dynamic power-up systems, and an unpredictable AI designed to challenge the player's strategic use of abilities.

---

### 🎮 Play the Game

**The latest stable build is available on itch.io:** 👉 **[Play Atomic Racers on itch.io](https://empiric-team.itch.io/atomic-racers)**

---

### 📑 Technical & Design Overview

The primary challenge of this project was building a cohesive racing experience from scratch without a commercial engine. As a programmer, I was responsible for building a fully functional ECS system from scratch, optimized to handle hundreds of entities without impacting game performance, and fully scalable. I also helped implement an online engine that allows you to compete with your friends, and I modeled and textured the models used in the game.

---

### 🚀 Key Systems & My Contributions

Our custom C++ engine follows an **ECS (Entity Component System)** architecture. In this data-driven structure, entities are collections of data, components store that data, and systems process it. While I contributed to several areas of the engine, I specialized in the following systems:

#### 🧩 Custom ECS Architecture
Instead of using conventional Object-Oriented Programming (OOP), I engineered a high-performance **ECS structure** designed for maximum organization, flexibility, and scalability.

* **⚙️ Metaprogramming & Optimization:** Leveraged **templates** and custom-built **slotmaps** to manage components, systems, and entities. By handling core logic during compilation, we minimized runtime overhead and drastically boosted execution efficiency.
* **📈 Scalability:** Designed a streamlined workflow where adding new entities is as simple as using pre-created templates, ensuring the system remains maintainable as the project grows.
* **🏭 Factory Pattern:** The Factory pattern was also used to decentralize entity creation and assign these responsibilities correctly; thus, the Entity Manager is solely responsible for managing them and does not have to create them.
* **🔗 Code Highlight:**
    * 📂 [`EntityManager.tpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/man/EntityManager.tpp) — Core logic for entity lifecycle and slotmap management.
    * 📂 [`Meta.hpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/util/Meta.hpp) & [`Meta.tpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/util/Meta.tpp) — Entity management through metaprogramming.
    * 📂 [`Slotmap.tpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/man/Slotmap.tpp) — Slotmap logic.
    * 📂 [`EntityFactoy.cpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/man/EntityFactory.cpp) — Entity management through metaprogramming.
    * 📂 [`Components Folder`](https://github.com/octavioo09/Atomic-Racers/tree/main/src/components) — Folder containing all components that manage entities.
    * 📂 [`System Folder`](https://github.com/octavioo09/Atomic-Racers/tree/main/src/system) — Folder where components are updated via systems.

#### 🌐 Asynchronous Network Engine
To elevate the project's capabilities, I developed a custom online engine from scratch using **Asio**, focused on security and efficient data distribution through a centralized architecture.

* **🛡️ Security & Reliability:** Implemented **encrypted message handling** within a client-server structure, ensuring that all data exchange is protected and validated by a central authority.
* **⚡ Traffic Optimization:** Designed a synchronization model where only essential state data is transmitted. This allows clients to **locally simulate** other players' driving, drastically reducing packet frequency and preventing I/O queue congestion.
* **🖥️ Centralized Management:** Engineered a robust server logic capable of triaging different message types and distributing them selectively to the relevant peers to minimize bandwidth overhead.
* **🔗 Code Highlight:**
    * 📂 [`net_message.h`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/net/net_message.h) — Format of the message types and their content structure.
    * 📂 [`net_client.h`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/net/net_client.h) — The player sends the appropriate type of message to the server.
    * 📂 [`net_server.h`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/net/net_server.h) — Message distribution and player state synchronization logic.
    * 📂 [`net_connection.h`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/net/net_connection.h) — Player connections and their encryption using a dynamic hash.

#### 🎨 3D Generalist & Environment Art
I took charge of the visual pipeline, ensuring a cohesive aesthetic between the high-speed vehicles and the world they inhabit.

* **🖌️ Asset Creation & Texturing:** Modeled and textured a significant portion of the game’s environment and the car models, maintaining a consistent art style and performance-friendly geometry.
* **🔍 Visual Check:** To see these assets in action, I invite you to **[play the final version here](https://empiric-team.itch.io/atomic-racers)**.

---

### 🛠️ Additional Technical Features
Beyond core architecture and networking, I implemented several key gameplay systems:

* **✨ Particle System from Scratch:** Developed a custom particle engine for visual effects like smoke, sparks, and speed trails.
* **🏁 Dynamic Waypoint System:** Engineered a fully dynamic pathfinding system to manage AI navigation and race progress.
* **⚡ Power-Up Framework:** Designed the logic for the game's power-ups, ensuring seamless integration with the ECS and network synchronization.
* **🔗 Code Highlight:**
    * 📂 [`ParticlesComponent.cpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/components/ParticlesComponent.cpp) & [`ParticlesSystem.cpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/system/ParticleSystem.cpp)
    * 📂 [`WaypointComponent.cpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/components/WaypointComponent.cpp)
    * 📂 [`PowerUpSystem.cpp`](https://github.com/octavioo09/Atomic-Racers/blob/main/src/util/CollisionInBroadphase.cpp)

---

### ✉️ Contact and Feedback
* **GitHub:** [octavioo.09](https://github.com/octavioo09)
* **LinkedIn:** [Octavio Vicent Lloret](https://www.linkedin.com/in/octavioo09/)
* **Email:** octaviovlloret@gmail.com



