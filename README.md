# 🕸️ OrgGraph – Interactive Dependency Visualizer

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)

**OrgGraph** is a high-performance interactive dashboard designed to visualize complex organizational structures, team dependencies, and potential bottlenecks.

Built to solve the **“hairball problem”** in graph visualization, OrgGraph allows managers and engineers to seamlessly switch between granular user-level views and high-level departmental clusters.

## 🚀 Key Features

- **📊 Interactive Physics Graph**  
  Draggable nodes with real-time physics simulation using `vis-network`.

- **🧩 Smart Clustering**  
  Toggle between **User Mode** and **Department Mode** to visualize cross-team dependencies.

- **🔍 Advanced Filtering**  
  Isolate specific relationship types such as *Critical Dependencies* or *Collaborations*.

- **📉 Real-time Analytics**  
  Dynamic stats panel showing total nodes, edges, and the *most connected* user.

- **📸 High-Resolution Export**  
  Canvas-to-image export that downloads the current graph state as a PNG.

- **🎨 Dynamic SVG Avatars**  
  Programmatically generated SVG avatars prevent canvas tainting and ensure secure exports.

---

## 🛠️ Tech Stack

- **Frontend:** React 18, TypeScript  
- **Build Tool:** Vite  
- **Visualization:** Vis.js (`vis-network`, `vis-data`)  
- **Styling:** Tailwind CSS  
- **Icons:** Lucide React  

---

## ⚙️ Getting Started

### Prerequisites
- Node.js v16 or higher
- npm

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/rajashree-shan/OrgGraph.git
   cd dependency-graph
2. npm install
3. npm run dev
4. Open http://localhost:5173 in your browser.
## Technical Highlights:
This project demonstrates several advanced frontend engineering concepts:
1. Imperative Library Integration:
Integrated the imperative vis.js graph engine into React’s declarative lifecycle using useRef and useEffect, preventing memory leaks and duplicate canvas renders.
2. Efficient Data Transformation:
Implemented a custom clustering algorithm with O(n) complexity to dynamically group users into departments, significantly reducing visual clutter.
3. Canvas Security & Exporting"
Solved browser Canvas Tainting issues by generating avatars as SVG Data URIs instead of fetching external images, enabling reliable toDataURL() exports.
<img width="1710" height="985" alt="image" src="https://github.com/user-attachments/assets/625e44c3-60f4-4cd3-a32a-ddaaf78a138f" />
<img width="1710" height="985" alt="image" src="https://github.com/user-attachments/assets/c7a43ba0-7f33-4d2e-b41d-2cde942aead0" />


## Future Improvements
[ ] Shortest Path Algorithm: Implement BFS to highlight the quickest connection between two selected nodes.

[ ] JSON Import: Allow users to upload their own .json dataset to visualize their own teams.

[ ] 3D Rendering: Experiment with Three.js for a 3D view of the network.

📄 License
This project is licensed under the MIT License.
