```markdown
# 🕸️ OrgGraph - Interactive Dependency Visualizer

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)

**OrgGraph** is a high-performance interactive dashboard designed to visualize complex organizational structures, team dependencies, and potential bottlenecks. 

Built to solve the "hairball problem" in data visualization, it allows managers and engineers to switch between granular user-level views and high-level departmental clusters.

![Project Screenshot](./dependency-graph.png)
*(Note: Use the 'Export Graph' button in the app to generate this image, then rename it to dependency-graph.png and push it to your repo)*

## 🚀 Key Features

* **📊 Interactive Physics Graph:** Draggable nodes with real-time physics simulation using `vis-network`.
* **🧩 Smart Clustering:** Toggle between individual "User Mode" and aggregated "Department Mode" to visualize cross-team dependencies.
* **🔍 Advanced Filtering:** Isolate specific relationship types (e.g., "Critical Dependencies" vs. "Collaborations").
* **📉 Real-time Analytics:** A dynamic stats panel showing total nodes, edges, and identifying the "Most Connected" user.
* **📸 High-Res Export:** Custom canvas-to-image generation allowing users to download the current graph state as a PNG.
* **🎨 Dynamic SVG Generation:** Avatars are generated programmatically to prevent Canvas Tainting and ensure secure exports.

## Tech Stack

* **Core:** React 18, TypeScript
* **Build Tool:** Vite
* **Visualization:** Vis.js (vis-network, vis-data)
* **Styling:** Tailwind CSS
* **Icons:** Lucide React

## Getting Started

### Prerequisites
* Node.js (v16 or higher)
* npm

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/yourusername/dependency-graph.git](https://github.com/yourusername/dependency-graph.git)
    cd dependency-graph
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Run the development server**
    ```bash
    npm run dev
    ```

4.  Open `http://localhost:5173` in your browser.

## Technical Highlights (Interview Notes)

This project demonstrates several advanced frontend concepts:

1.  **DOM Integration with React:**
    * Integrated an imperative library (`vis.js`) into the declarative React lifecycle using `useRef` and `useEffect`, ensuring no memory leaks or duplicate canvas renders.
    
2.  **Data Transformation:**
    * Implemented a custom grouping algorithm that reduces the graph complexity by `O(n)` to cluster users into departments dynamically.

3.  **Canvas Security & Exporting:**
    * Solved the browser "Canvas Tainting" security issue by generating SVG avatars programmatically (Data URIs) instead of fetching external CORS-blocked images. This allows the `toDataURL()` export function to work seamlessly.

## Project Structure

```text
src/
├── App.tsx          # Main Application Logic (State, Graph Config, UI)
├── data.ts          # Data Layer & SVG Generation Utility
├── main.tsx         # Entry Point
└── index.css        # Tailwind Imports & Custom Scrollbars

```

<img width="1710" height="985" alt="image" src="https://github.com/user-attachments/assets/a16b68b2-534b-4b8b-9477-e81fe241da7a" />

<img width="1710" height="985" alt="image" src="https://github.com/user-attachments/assets/f1716baa-6b05-438d-8b78-bac170fe344b" />

## Future Improvements

* [ ] **Shortest Path Algorithm:** Implement BFS to highlight the quickest connection between two selected nodes.
* [ ] **JSON Import:** Allow users to upload their own `.json` dataset to visualize their own teams.
* [ ] **3D Rendering:** Experiment with `Three.js` for a 3D view of the network.

## License

This project is open source and available under the [MIT License](https://www.google.com/search?q=LICENSE).

```

```
