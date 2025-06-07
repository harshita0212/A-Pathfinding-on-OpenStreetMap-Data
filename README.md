

## 📌 Project Description — Route Planning using A\* on OpenStreetMap

This project implements a **C++ application** that performs **route planning** on real-world map data using the **A* search algorithm*\*. The map data is sourced from **OpenStreetMap (OSM)**, and the graphical rendering is done using the **IO2D** graphics library.

The goal of the application is to find the **shortest path between two points** (start and end coordinates) on a real map and **visually display the computed path** using a graphical interface.

---

### 🔍 Key Features

* 📍 **Real Map Data**: Uses `.osm` files (OpenStreetMap XML format) to load map structures including roads, intersections, and paths.
* 🚗 **A* Search Algorithm*\*: Efficient heuristic-based pathfinding, balancing path cost and distance to goal.
* 🎨 **2D Graphical Visualization**: Uses IO2D (a 2D graphics library) to render the map and animate the shortest path.
* ⚙️ **Customizable Input**: Users can select different start and end coordinates directly from the UI or through command line.
* 🧪 **Unit Testing**: Includes test cases to verify correctness of components like distance calculation, node sorting, neighbor finding, etc.

---

### 🧠 Learning Objectives (from Udacity C++ Nanodegree)

* ✳️ Object-Oriented Design and Encapsulation
* ✳️ Memory management (pointers, references, object lifetime)
* ✳️ Working with third-party libraries (IO2D, CMake)
* ✳️ Modern C++ features (smart pointers, lambda functions, range-based loops)
* ✳️ Implementing algorithms from scratch (A\* pathfinding)

---

## ⚙️ Requirements

* **WSL (Ubuntu)** on Windows
* **VS Code with WSL extension**
* **CMake ≥ 3.11**
* **g++ ≥ 7.4**
* **make**
* **IO2D graphics library**

---

## 🔧 Step-by-Step Installation

### 🔹 1. Open Terminal in WSL (Ubuntu)

Make sure you're inside WSL:

```bash
wsl
```

---

### 🔹 2. Install Build Dependencies

```bash
sudo apt update
sudo apt install build-essential cmake g++ libcairo2-dev libgraphicsmagick1-dev libpng-dev -y
```

---

### 🔹 3. Install IO2D Library

```bash
cd ~
git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
cd P0267_RefImpl
mkdir Debug
cd Debug
cmake -DCMAKE_BUILD_TYPE=Debug ..
cmake --build .
sudo make install
```

---

### 🔹 4. Clone This Project

```bash
cd ~
git clone --recurse-submodules https://github.com/YourUsername/route-planning-main.git
cd route-planning-main
```

Or if you already have the folder from ZIP:

```bash
cd ~
mv ~/Downloads/route-planning-main ~/route-planning-main
cd route-planning-main
```

---

## 🧱 Build Instructions

```bash
mkdir build
cd build
cmake ..
make
```

> If IO2D is correctly installed, this will build the app.

---

## 🚀 Run the Application

```bash
./OSM_A_star_search
```

To run with a custom map:

```bash
./OSM_A_star_search -f ../map.osm
```

Make sure `map.osm` is placed inside the main `route-planning-main/` folder.

---

## 🧪 Run Tests

If the test binary was compiled:

```bash
./test
```

---

## 🗺️ Download a Map File (if needed)

You can use this sample map (Berlin):
[https://raw.githubusercontent.com/udacity/CppND-Route-Planning-Project/master/map.osm](https://raw.githubusercontent.com/udacity/CppND-Route-Planning-Project/master/map.osm)

Download using:

```bash
wget https://raw.githubusercontent.com/udacity/CppND-Route-Planning-Project/master/map.osm
```

Place it in the root of the `route-planning-main` folder.

---

## ✅ Folder Structure

```
route-planning-main/
├── build/
├── map.osm
├── CMakeLists.txt
├── src/
└── README.md
```

---

### 🖼️ Sample Output (Visual)

> 🚀 A visual window pops up displaying the map with a red path traced from the start to the goal node — all computed using A\*!

---

