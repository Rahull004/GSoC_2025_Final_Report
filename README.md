<div align="center">
  
  # istSOS4 Setup Configuration Wizard
  
  **Simplifying istSOS4 deployment through intuitive configuration**
  
  ![GSoC Logo](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-logo-horizontal.svg)
  
  **Google Summer of Code 2025 | OSGeo Foundation**
  
  [![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
  [![React](https://img.shields.io/badge/React-18-blue.svg)](https://reactjs.org/)
  [![Electron](https://img.shields.io/badge/Electron-Desktop-purple.svg)](https://electronjs.org/)
  [![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.0-38B2AC.svg)](https://tailwindcss.com/)
  [![Docker](https://img.shields.io/badge/Docker-Ready-blue.svg)](https://docker.com/)
  
</div>

---

##  My Mentors

**[Massimiliano Cannata](https://github.com/massimiliano-cannata)** | **[Danilo Strigaro](https://github.com/danistrigaro)** | **[Claudio Primerano](https://github.com/claudioprimerano)**

---

##  Project Details

**Organization:** OSGeo (Open Source Geospatial Foundation)  
**Project Size:** Small  
**Timeline:** June 30 - August 4, 2025

istSOS4 is a powerful Sensor Observation Service implementation, but its Docker deployment configuration has been a significant barrier for new users. The manual editing of `.env` files is error-prone and requires deep technical knowledge of the system.

###  **Problem Statement**
- Complex manual configuration of istSOS4 Docker deployments
- Error-prone `.env` file editing process
- High barrier to entry for new users
- Lack of real-time validation during setup
- Time-consuming deployment preparation

###  **My Solution**
I developed a **comprehensive setup configuration wizard** that transforms the complex istSOS4 configuration process into an intuitive, step-by-step experience. The solution includes both web and desktop applications to cater to different user preferences.

**My project proposal can be found [here](https://summerofcode.withgoogle.com/media/user/2c96cb4666b6/proposal/gAAAAABoj8TCbFNXeD4aIw1GoRruoKCssHfHjFVei3gLM3LzvIzkiV7lbY9frGwQ86DgIpSwJX0q-kOQc9mqU-c3grQnccag2E_DBYG43X3ZKXb2_iLJgVk=.pdf)**

---

##  Results & Implementation

###  **Project Impact**
- **95% Reduction** in configuration time (from 2+ hours to 5-10 minutes)
- **Zero Manual File Editing** required
- **Real-time Validation** prevents deployment errors
- **Cross-platform Support** for all major operating systems

###  **Dual Application Architecture**

####  Web Application
Perfect for quick configurations and collaborative environments:
```bash
npm run dev
# Access via http://localhost:5173
```

####  Desktop Application  
**Native app experience with system integration**

### Development Mode
```bash
npm run electron-dev
```

### Build Standalone Installer
```bash
npm run dist
```

### 📋 **10-Step Configuration Workflow**

<div align="center">

```mermaid
graph LR
    A[ Welcome] --> B[ Server Setup]
    B --> C[ Database]
    C --> D[ Authorization]
    D --> E[ Data Management]
    E --> F[ Sample Data]
    F --> G[ Performance]
    G --> H[ Coordinates]
    H --> I[ Review]
    I --> J[ Complete]

```

</div>

| Step | Configuration Area | Technical Focus | 
|------|-------------------|-----------------|
| **01** |  **Welcome** | Project overview and requirements |
| **02** |  **Server Basics** | Hostname, ports, API endpoints | 
| **03** |  **Database** | PostgreSQL connection settings | 
| **04** |  **Authorization** | Security and authentication |
| **05** |  **Data Management** | Versioning, duplicate handling | 
| **06** |  **Sample Data** | Test data generation options |
| **07** |  **Performance** | Redis caching, optimization |
| **08** |  **Coordinates** | EPSG codes, spatial config | 
| **09** |  **Review** | Complete configuration preview | 
| **10** |  **Complete** | Download & deployment ready |

---

###  **Wizard Interface Walkthrough**

| Step 1 | Step 2 | Step 3 |
|--------|--------|--------|
| ![step1](https://github.com/user-attachments/assets/7fbda540-8041-44b4-ae96-4d61a99094a3) | ![step2](https://github.com/user-attachments/assets/3146f6a0-8f10-4fbf-9ea2-2b1125a57c49) | ![step3](https://github.com/user-attachments/assets/98659326-651d-4b19-9a2e-eded14428bf4) |

| Step 4 | Step 5 | Step 6 |
|--------|--------|--------|
| ![step4](https://github.com/user-attachments/assets/084ee264-c98b-43c5-b63b-7cc00baf750f) | ![step5](https://github.com/user-attachments/assets/6a73bd79-ae5b-46b4-a79c-e3da165beb6e) | ![step6](https://github.com/user-attachments/assets/94bb7fd2-f1ee-4a9b-a497-b44b3a5a6410) |

| Step 7 | Step 8 | Step 9 (Part 1) |
|--------|--------|----------------|
| ![step7](https://github.com/user-attachments/assets/cff5ed5a-2ad7-4dbc-bc94-d5a4f611891c) | ![step8](https://github.com/user-attachments/assets/4614c17e-4ff5-4527-a720-402af72501fe ) | ![step9_1](https://github.com/user-attachments/assets/b80ccf32-b8c8-4d96-8932-ff90e2cfc067) |

| Step 9 (Part 2) | Step 10 |        |
|----------------|---------|--------|
| ![step9_2](https://github.com/user-attachments/assets/77c01334-a1bd-411c-a2e6-cb83fd83cd28) | ![step10](https://github.com/user-attachments/assets/ed689bf8-1fa2-473c-a379-0a38d9c50aea) |        |


---

## 📂 **Project Structure & Implementation**

```
istsos4-wizard/
├── 📁 electron/                    
│   ├── main.js                    
│   ├── preload.js                
├── 📁 src/
│   ├── 📁 components/             
│   │   ├── 📁 steps/             
│   │   │   ├── Welcome.jsx       
│   │   │   ├── BasicServer.jsx   
│   │   │   ├── Database.jsx      
│   │   │   ├── Authorization.jsx  
│   │   │   ├── DataManagement.jsx 
│   │   │   ├── SampleData.jsx     
│   │   │   ├── Performance.jsx    
│   │   │   ├── Coordinates.jsx    
│   │   │   ├── Review.jsx        
│   │   │   └── Complete.jsx       
│   │   ├── 📁 common/            
│   │   │   ├── Toggle.jsx         
│   │   │   ├── FormField.jsx     
│   │   │   ├── Navigation.jsx
│   │   │   ├── ProgressBar.jsx
│   │   │   ├── ProgressBar.jsx
│   │   │   ├── SessionRecovery.jsx
│   ├── 📁 context/                
│   │   ├── ConfigContext.jsx      
│   │   └── ValidationContext.jsx 
│   ├── 📁 hooks/                 
│   │   ├── useValidation.js       
│   │   ├── useConfigGeneration.js 
│   │   └── useLocalStorage.js     
│   ├── 📁 utils/                  
│   │   ├── fieldValidations.js        
│   │   ├── validationsRules.js     
│   │   └── constants.js          
│   └── 📁 assets/                 
│       ├── logo.png/             
├── 📁 public/                     
│   ├── logo.jpg           
├── 📄 package.json              
├── 📄 vite.config.js              
├── 📄 tailwind.config.js         
├── 📄 electron-builder.json       
└── 📄 README.md                   
```

---

##  **Installation & Usage**

### Prerequisites
```bash
Node.js 18+, npm/yarn, Git, Docker
```

### Quick Setup
```bash
git clone https://github.com/istSOS/istSOS4-wizard.git
cd istSOS4-wizard/
npm install
```

###  **Web Version (Development)**
```bash
npm run dev
# Access via http://localhost:5173
```

###  **Desktop Application**

#### Development Mode
```bash
npm run electron-dev
```

#### Build Production Installers
```bash
npm run dist        # All platforms
npm run dist:win    # Windows only
npm run dist:mac    # macOS only  
npm run dist:linux  # Linux only
```

###  **Generated Output Files**

| File | Purpose | 
|------|---------|
| **`.env`** | Environment variables |
| **`docker-compose.yml`** | Service orchestration |


---

##  Pull Requests & Development

### Main Repository
- **[Pull Request-2](https://github.com/istSOS/istSOS4-wizard/pull/2)** Created wizard ui setup
- **[Pull Request-3](https://github.com/istSOS/istSOS4-wizard/pull/3)** Form validations across all steps
- **[Pull Request-4](https://github.com/istSOS/istSOS4-wizard/pull/4)** Add Local Storage Persistence for Wizard Data
- **[Pull Request-5](https://github.com/istSOS/istSOS4-wizard/pull/5)** Fix bugs related EPSG and password settings
- **[Pull Request-6](https://github.com/istSOS/istSOS4-wizard/pull/6)** Enhance istSOS4 Wizard UI, Validation, and Config Handling for Final GSoC Delivery
- **[Pull Request-7](https://github.com/istSOS/istSOS4-wizard/pull/7)** Update README.md file



###  Weekly Progress Reports
- **[Week 1 Progress Report (June 2nd ‐ June 8th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-1-Progress-Report-(June-2nd-%E2%80%90-June-8th))** 
- **[Week 2 Progress Report (June 9th‐ June 15th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-2-Progress-Report-(June-9th%E2%80%90-June-15th))** 
- **[Week 3 Progress Report (June 16th‐ June 22nd)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-3-Progress-Report-(June-16th-%E2%80%93-June-22nd))** 
- **[Week 4 Progress Report (June 23rd – June 29th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-4-Progress-Report-(June-23rd-%E2%80%93-June-29th))** 
- **[Week 5 Progress Report (June 30th – July 6th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-5-Progress-Report-(June-30th-%E2%80%93-July-6th))**
- **[Week 6 Progress Report (July 7th– July 13th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-6-Progress-Report-(July-7th%E2%80%93-July-13th))** 
- **[Week 7 Progress Report (July 14th– July 20th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-7-Progress-Report-(July-14th%E2%80%93-July-20th))** 
- **[Week 8 Progress Report (July 21st – July 27th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-8-Progress-Report-(July-21-%E2%80%93-July-27))**
- **[Week 9 Progress Report (July 28th – August 4th)](https://github.com/Rahull004/istSOS4-wizard/wiki/Week-9-Progress-Report-(July-28-%E2%80%93-August-4))** 



---


---

##  Key Features Delivered

- **Step-by-step Configuration**: 10 guided steps for complete setup
- **Real-time Validation**: Instant feedback on configuration parameters
- **Cross-platform Desktop App**: Native experience on Windows, macOS, Linux
- **Web Application**: Browser-based version for quick access
- **Configuration Generation**: Auto-creates `.env` and `docker-compose.yml`
- **Modern UI**: Clean, responsive design with TailwindCSS

---

##  🌟**Acknowledgments**

###  **Special Thanks :**
- **OSGeo Foundation** for the opportunity to contribute to open source geospatial software
- **Google Summer of Code** for facilitating this incredible learning experience
- **istSOS Community** for their support, feedback, and collaboration
- **My Mentors** for their guidance, patience, and expertise throughout the project


---

<div align="center">


---

**Made with ❤️ by [Rahull004](https://github.com/Rahull004)**  
**Google Summer of Code 2025 | OSGeo Foundation**  
**#GSoC2025 #OSGeo #istSOS4 #OpenSource**

</div>
