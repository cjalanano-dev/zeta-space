**Project Overview** VIBE is an immersive, 3D web application designed to transform audio input into a dynamic and mesmerizing visual experience in real-time. Built on the modern React ecosystem, it bridges the gap between signal processing and 3D graphics, creating a synchronized audiovisual environment where geometry and lighting respond instantly to sound frequencies.

**Technical Architecture**

- **Audio Signal Processing:** The core engine leverages the browser's Web Audio API and `AnalyserNode` to perform real-time frequency analysis on incoming audio streams. It deconstructs the audio signal into distinct frequency bands (Bass, Mid, and Treble) to drive specific visual elements independently.
    
- **3D Graphics Pipeline:** Rendering is handled by Three.js, abstracted through `@react-three/fiber` to allow for a declarative, component-based scene graph. This architecture enables efficient updates to 3D primitives (meshes, lights, and cameras) synchronous with the audio frame rate.
    
- **Post-Processing:** The visual output is enhanced via a post-processing pipeline (`@react-three/postprocessing`), specifically utilizing Bloom effects to create a glowing, neon aesthetic that intensifies with audio amplitude.
    

**Key Features**

- **Dual Input Modes:** Supports seamless switching between live audio input (Microphone/Ambient) and local file playback (MP3/Audio files), managing audio context lifecycles for both sources.
    
- **Frequency-Mapped Visuals:**
    
    - **Bass Response:** A central sphere pulses and shifts color intensity based on low-end frequencies.
        
    - **Mid-Range Dynamics:** A rotating torus ring modulates its spin speed in sync with mid-range beats.
        
    - **Treble Reactivity:** Floating particulate elements react to high-frequency transients.
        
- **Modern User Interface:** Features a "Glassmorphism" UI overlay with dark mode aesthetics, providing intuitive controls for volume, playback, and source selection without obstructing the visualizer.
    

**Tech Stack**

- **Core Framework:** React 19
    
- **Build Tool:** Vite
    
- **3D Engine:** Three.js, @react-three/fiber
    
- **Helpers & Abstractions:** @react-three/drei
    
- **Effects:** @react-three/postprocessing
    
- **Language:** JavaScript (ES Modules)