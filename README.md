# React Tree Nav 🌳

A high-density, hierarchical timeline component for React. It flattens complex tree structures into a sleek, linear "Fish-Eye" navigation bar.

![Timeline Demo](https://via.placeholder.com/800x200?text=Tree+Nav+Preview)

## 🌟 Why?

Standard progress bars are linear (`1 -> 2 -> 3`). But real-world flows are hierarchical trees:
-   **SaaS Config**: Account → Settings → **Billing (20 fields)** → Team
-   **Learning**: Course → Module → **Lesson (10 steps)** → Quiz
-   **Forms**: Loan App → Assets → **Financials (15 docs)** → Review

**React Tree Nav** solves this by allowing users to:
1.  **Drill Down** into nested branches without losing context.
2.  **Interact** with massive lists (20+ items) using a smart "Fish-Eye" expand-on-hover.
3.  **Navigate** granular sub-steps (fields/questions) directly from the parent view.

## ✨ Key Features

-   **🐟 Fish-Eye Zoom**: Hover over any segment in a crowded list to expand it instantly.
-   **💊 Micro-Steps**: Visualize granular progress (e.g., "Question 4 of 10") within a single parent step.
-   **🪜 Smart Breadcrumbs**: "Back" button that understands your traversal path.
-   **🛡️ Mouse Trap**: Intelligent delays prevent accidental clicks during rapid movement.
-   **🎹 Keyboard Ready**: Full arrow-key navigation and focus management.

## 🎮 Use Cases

### 1. Complex Wizards (FinTech / Gov)
Perfect for **Loan Applications** or **Tax Filings** where specific sections (like "Financial History") explode into 20+ sub-tasks. Users can jump back to "Document 4" instantly.

### 2. Learning Management Systems (LMS)
Replace clunky sidebar trees. Students can see they are in "Week 4 > Quiz 2" and scrub through questions without leaving the lesson view.

### 3. SaaS Settings & Onboarding
Great for "Setup Guides" where steps like "API Configuration" have many sub-toggles.

### 4. Order Tracking & Logistics
Visualize "Order Placed → Processing → **In Transit (15 hops)** → Delivered" in one clean bar.

## 📦 Installation

*(Coming Soon to npm)*

```bash
npm install react-tree-nav
```

## 💻 Quick Start

```jsx
import { TreeNav } from 'react-tree-nav';

const myData = {
  '1': { id: '1', title: 'Intro', type: 'slide', duration: 10 },
  '2': { id: '2', title: 'Setup', type: 'navigation', duration: 0 }, // Has children
  '2.1': { id: '2.1', title: 'Install Node', type: 'slide', parent: '2', narrations: 3 },
  // ...
};

function App() {
  return (
    <TreeNav
      data={myData}
      onNavigate={(nodeId) => console.log('Navigated to', nodeId)}
    />
  );
}
```

## 🛠️ Tech Stack

-   **React 18**
-   **Tailwind CSS** (styling)
-   **Lucide React** (icons)

## 📄 License

MIT
