# 🎴 3D FlashCard Interactive Learning Experience

> An immersive 3D flashcard application built with React Three Fiber that transforms traditional learning into an engaging visual experience with physics-based interactions and custom 3D geometries.

![React](https://img.shields.io/badge/React-19.0.0-61DAFB?style=for-the-badge&logo=react&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-0.176.0-000000?style=for-the-badge&logo=three.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.7.2-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-6.3.1-646CFF?style=for-the-badge&logo=vite&logoColor=white)

## ✨ Features

- **🌐 3D Interactive Cards**: Stunning 3D card animations powered by React Three Fiber
- **⚛️ Physics Simulation**: Realistic card physics using Rapier physics engine
- **🎯 Tech Knowledge Base**: 30 curated programming and web development questions
- **🎨 Custom Geometries**: Hand-crafted rounded plane geometries for smooth card edges
- **📝 Dynamic Text Rendering**: 3D text generation for questions and answers
- **🖼️ Custom Textures**: Real-time canvas-based texture generation for card faces
- **🎮 Interactive Controls**: Intuitive UI controls for navigating flashcards
- **📱 Responsive Design**: Optimized for all screen sizes
- **⚡ Lightning Fast**: Built with Vite for optimal performance and hot module replacement


## 🚀 Quick Start

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/3d-flashcard-learning.git

# Navigate to project directory
cd 3d-flashcard-learning

# Install dependencies
npm install

# Start development server
npm run dev
```

Visit `http://localhost:5173` to see the app in action!

## 📦 Tech Stack

| Technology | Purpose |
|------------|---------|
| **React 19** | UI Framework with latest features |
| **Three.js** | WebGL 3D Graphics Engine |
| **React Three Fiber** | React Renderer for Three.js |
| **React Three Drei** | Useful helpers and abstractions for R3F |
| **React Three Rapier** | Physics Engine Integration |
| **TypeScript** | Static Type Checking |
| **Vite** | Build Tool & Dev Server |
| **MeshLine** | Advanced line rendering in 3D |
| **JSBarcode** | Barcode generation capabilities |
| **QR Code Styling** | Custom QR code generation |

## 🏗️ Project Structure

```
flash-card-main/
├── node_modules/
├── public/
│   └── [static assets]
├── src/
│   ├── flashCard/
│   │   ├── components/
│   │   │   ├── Card.tsx                  # Main 3D card component with flip logic
│   │   │   ├── CardTexture.tsx           # Dynamic canvas texture generation
│   │   │   ├── CreateText.tsx            # 3D text mesh rendering
│   │   │   ├── Experience.tsx            # Main 3D scene setup & orchestration
│   │   │   └── FlashcardControls.tsx     # UI controls & navigation
│   │   ├── data/
│   │   │   └── database.ts               # 30 flashcard Q&A data
│   │   ├── lib/
│   │   │   └── RoundedPlaneGeometry.ts   # Custom geometry for rounded cards
│   │   ├── styles/
│   │   │   └── FlashcardControls.css     # Control panel styling
│   │   └── types/
│   │       └── types.d.ts                # TypeScript type definitions
│   ├── App.tsx                            # Root application component
│   ├── main.tsx                           # Application entry point
│   └── index.css                          # Global styles
├── .gitignore
├── .hintrc
├── eslint.config.js                       # ESLint configuration
├── index.html                             # HTML entry point
├── package.json                           # Dependencies & scripts
├── package-lock.json
├── tsconfig.json                          # TypeScript configuration
├── tsconfig.app.json                      # App-specific TS config
├── tsconfig.node.json                     # Node-specific TS config
├── vite.config.ts                         # Vite build configuration
└── README.md
```

## 🎮 How It Works

### Component Architecture

1. **Experience.tsx**: Sets up the 3D scene, camera, lighting, and physics world
2. **Card.tsx**: Renders individual 3D flashcards with flip animations and physics bodies
3. **CardTexture.tsx**: Generates dynamic canvas textures for card faces (question/answer)
4. **CreateText.tsx**: Renders 3D text meshes using Three.js text geometry
5. **FlashcardControls.tsx**: Provides navigation buttons and current card indicator
6. **RoundedPlaneGeometry.ts**: Custom geometry class for smooth, rounded card edges

### User Interactions

- **Navigate Cards**: Use arrow buttons or keyboard controls to move through cards
- **Flip Cards**: Click on a card or press spacebar to reveal the answer
- **3D Manipulation**: Drag and rotate cards in 3D space
- **Physics**: Cards respond to physics forces for realistic movement

## 📚 Flashcard Topics Covered

The app includes 30 essential programming concepts:

- **JavaScript Core**: Closures, Promises, Async/Await, Type Coercion
- **Web Fundamentals**: HTML, CSS, DOM, JSON
- **React Ecosystem**: Components, Hooks, Virtual DOM
- **TypeScript**: Static Typing, Type Safety
- **Data Structures**: Stacks, Queues, Big O Notation
- **Backend**: Node.js, APIs, RESTful Services, Middleware
- **Algorithms**: Recursion, Binary Search
- **Tools**: Git, IDEs, Frameworks

## 🛠️ Available Scripts

```bash
# Development
npm run dev          # Start dev server with hot reload

# Production
npm run build        # Compile TypeScript & build for production
npm run preview      # Preview production build locally

# Code Quality
npm run lint         # Run ESLint for code quality checks
```

## 🎨 Customization Guide

### Adding Custom Flashcards

Edit `src/flashCard/data/database.ts`:

```typescript
import { FlashCard } from "../types/types";

export const flashcards: FlashCard[] = [
    {
        question: "Your custom question?",
        answer: "Your detailed answer here"
    },
    // Add more cards...
];
```

### Styling the Cards

Modify card appearance in:
- **Card geometry**: `src/flashCard/lib/RoundedPlaneGeometry.ts`
- **Card textures**: `src/flashCard/components/CardTexture.tsx`
- **3D scene**: `src/flashCard/components/Experience.tsx`

### Customizing Controls

Update UI controls in:
- **Component**: `src/flashCard/components/FlashcardControls.tsx`
- **Styles**: `src/flashCard/styles/FlashcardControls.css`

### Adjusting Physics

Modify physics parameters in `Experience.tsx`:
- Gravity strength
- Collision detection
- Restitution (bounciness)
- Friction

## 🔧 Configuration Files

- **vite.config.ts**: Vite build configuration and plugins
- **tsconfig.json**: Base TypeScript compiler options
- **tsconfig.app.json**: App-specific TypeScript settings
- **eslint.config.js**: ESLint rules and configuration
- **.hintrc**: Browser compatibility hints

## 🌟 Key Features Breakdown

### 1. Custom 3D Geometry
Uses `RoundedPlaneGeometry` for smooth, rounded card edges that look professional

### 2. Dynamic Texture Generation
`CardTexture.tsx` creates textures on-the-fly using HTML5 Canvas API

### 3. Physics Integration
Rapier physics engine provides realistic card movement and collisions

### 4. Type Safety
Full TypeScript support with custom type definitions in `types.d.ts`

### 5. Modern Build Pipeline
Vite provides instant HMR and optimized production builds

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🐛 Report bugs
2. 💡 Suggest new features
3. 📝 Improve documentation
4. 🎨 Enhance UI/UX
5. ➕ Add more flashcard questions

### Steps to Contribute

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🐛 Known Issues

- None at the moment! Report any bugs in the Issues section.

## 🚀 Future Enhancements

- [ ] Add sound effects for card flips
- [ ] Implement spaced repetition algorithm
- [ ] Add progress tracking and statistics
- [ ] Support for multiple flashcard decks
- [ ] User authentication and cloud sync
- [ ] Mobile touch gesture support
- [ ] Dark/Light theme toggle
- [ ] Export/Import flashcard sets

## 🙏 Acknowledgments

- [React Three Fiber](https://docs.pmnd.rs/react-three-fiber) - Amazing 3D React integration
- [Three.js](https://threejs.org/) - Powerful WebGL 3D library
- [Rapier](https://rapier.rs/) - Blazing fast physics engine
- [Vite](https://vitejs.dev/) - Next generation frontend tooling
- [Drei](https://github.com/pmndrs/drei) - Useful React-Three-Fiber helpers

## 📧 Contact

Shashank Sharma 

Project Link: [https://github.com/Shashank09012003/3d-flashcard-learning](https://3-d-flash-card-interactive-learning.vercel.app/)

---

<p align="center">Built with ❤️ using React, Three.js & TypeScript</p>
<p align="center">⭐ Star this repo if you find it helpful!</p>
<p align="center">🔄 Fork it to create your own learning experience!</p>
