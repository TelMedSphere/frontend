 # <p align="center">💖TelMedSphere Frontend</p>

<div id="top"></div>

<h2>🧾 Table of Contents</h2>

 [📌 Introduction](#introduction).<br>
 [💡 Features](#features).<br>
 [🚀 Technology Stack](#technology-stack).<br>
 [🏗️ Project Structure](#project-structure).<br>
 [⭐ Overview](#overview).<br>
 [💥 Getting Started](#getting-started).<br>
 [🐳 Docker Setup](#docker-setup).<br>
 [🔌 Environment Variables](#environment-variables).<br>
<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>📌Introduction</h2>

TelMedSphere's frontend is built with React and provides a user-friendly interface for the telemedicine platform. It offers a seamless experience for both doctors and patients, allowing them to connect through video calls, manage health records, process payments, and handle prescriptions efficiently. The interface is designed to be intuitive, responsive, and accessible on various devices.

<h2>💡Features</h2>

🚨 For Patients:<br>
 - Book Video Calls: Easily schedule video consultations with doctors.
 - Share Feedback: Rate and review the doctor after your consultation.
 - Manage Your Profile: Update and view your personal details.
 - View Past Records: Check previous orders and prescriptions in one place.
 - Easy Payments: Use the wallet feature powered by Stripe for secure payments.
 
🚨 For Doctors:<br>
 - Set Up Your Profile: Add information about yourself and your services.
 - Manage Availability: Set your working hours for consultations.
 - Join Video Calls: Connect with patients at the scheduled time.
 - Write Prescriptions: Share prescriptions directly with patients after the consultation.
 - Queue System: Organize appointments efficiently with a smart queue feature.

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🚀Technology Stack</h2>

<p>
  <a href="https://www.w3schools.com/html/"> <img src="https://img.icons8.com/?size=64&id=20909&format=png" alt="HTML" /></a>
  <a href="https://www.w3schools.com/css/"> <img src="https://img.icons8.com/?size=64&id=21278&format=png" alt="CSS" /></a>
  <a href="https://www.w3schools.com/js/"> <img src="https://img.icons8.com/?size=64&id=108784&format=png" alt="JS" /></a>
  <a href="https://www.w3schools.com/REACT/DEFAULT.ASP"> <img src="https://img.icons8.com/?size=64&id=NfbyHexzVEDk&format=png" alt="React" /></a>
</p>

🚨 **Core Framework**: ReactJS <br>
🚨 **Build Tool**: Vite <br>
🚨 **Styling**: TailwindCSS <br>
🚨 **State Management**: React Context API <br>
🚨 **Routing**: React Router DOM <br>
🚨 **UI Components**: Material UI <br>
🚨 **Video Conferencing**: Jitsi <br>
🚨 **PDF Generation**: jsPDF <br>
🚨 **Animations**: Framer Motion <br>
🚨 **Notifications**: React-Toastify <br>
🚨 **Payment Processing**: Stripe <br>
🚨 **Containerization**: Docker <br>
🚨 **Deployment**: Vercel <br>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🏗️Project Structure</h2>

```
frontend/
├── public/               # Static assets
├── src/
│   ├── assets/           # Images and static resources
│   ├── components/       # Reusable UI components
│   │   ├── cart/         # Shopping cart components
│   │   ├── common/       # Shared components (header, footer, etc.)
│   │   ├── diseasePrediction/ # Disease prediction feature components
│   │   ├── facts/        # Health facts components
│   │   ├── form/         # Form components
│   │   ├── landingPage/  # Landing page specific components
│   │   ├── medicines/    # Medicine related components
│   │   ├── numberedCard/ # Numbered card components
│   │   ├── orders/       # Order management components
│   │   ├── pdfgenerator/ # PDF generation components
│   │   └── resetPassword/ # Password reset components
│   ├── contexts/         # React context providers
│   │   ├── cart/         # Cart context
│   │   ├── common/       # Shared contexts
│   │   ├── DarkMode/     # Theme context
│   │   └── filters/      # Filter contexts
│   ├── data/             # Static data and mock data
│   ├── hooks/            # Custom React hooks
│   ├── pages/            # Application pages
│   ├── routes/           # Route configurations
│   ├── App.jsx           # Main application component
│   ├── firebase.js       # Firebase configuration
│   ├── httpClient.js     # HTTP client for API calls
│   └── index.jsx         # Application entry point
├── .env.example          # Environment variables example
├── package.json          # Project dependencies and scripts
├── tailwind.config.js    # Tailwind CSS configuration
└── vite.config.js        # Vite configuration
```

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>⭐Overview</h2>

<h1 align="center"> <a href="https://pratik0112-telmedsphere.vercel.app/"> Live Project Demo ↗️</a></h1>

![](https://github.com/PratikMane0112/TelMedSphere/blob/master/Overview/1.png)

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->
<h2>💥Getting Started</h2>

- Fork this Repository.
- Clone the forked repository in your local system.
  
```bash
git clone https://github.com/TelMedSphere/frontend.git
```

<h2>💻Local Setup</h2>

Follow these steps to set up the frontend locally:
  
```bash
# Navigate to frontend directory
cd TelMedSphere/frontend

# Install all npm packages for react frontend
# Use `npm ci` to avoid changing package-lock.json after every install
npm ci

# Set up environment variables
cp .env.example .env
# (For Windows) copy .env.example .env

# Start the development server 
npm run dev
```

Once the development server is running, you can access the application at `http://localhost:3000` by default.

<h3>📝Available Scripts</h3>

In the project directory, you can run:

- `npm run dev`: Runs the app in development mode
- `npm run build`: Builds the app for production
- `npm start`: Previews the production build locally
<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

## How to Get `.env` File Variables

Refer to the [EnvVarSetUpGuideline.md](.github/EnvVarSetUpGuideline.md) for detailed steps on setting up the `.env` files for both the frontend and backend.


<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->
<h2>🐳Docker Setup</h2>

Docker provides an easier way to set up and run the frontend with all its dependencies.

### Prerequisites
- Docker [installed](https://www.docker.com/products/docker-desktop/) on your system
- Environment variables ready for configuration

### Steps to Run with Docker

1. Clone the repository as described above
2. Navigate to the frontend directory:
   ```bash
   cd TelMedSphere/frontend
   ```

3. Build and run the Docker container:
   ```bash
   docker build -t telmedsphere-frontend .
   docker run -p 3000:3000 telmedsphere-frontend
   ```

The frontend application will be available at:
- http://localhost:3000

### Using Docker Compose (Frontend only)

You can also use a simple Docker Compose setup for just the frontend:

```bash
# Create a docker-compose.yml file in the frontend directory with:
# ---
# version: '3'
# services:
#   frontend:
#     build: .
#     ports:
#       - "3000:3000"
# ---

# Then run:
docker-compose up --build
```

### Stopping the Container
```bash
# If using docker run
docker stop <container-id>

# If using docker-compose
docker-compose down
```

<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🔌Environment Variables</h2>

The frontend requires several environment variables to connect to the backend services. Create a `.env` file in the frontend directory with the following variables (refer to `.env.example`):

```
# Stripe Secret Key
VITE_PUBLICATION_KEY=your_stripe_secret_key

# Jitsi Key
VITE_JAAS_APP_ID=your_jitsi_meet_key

# API Key for chatbot
VITE_API_KEY = 'your_api_key'

# Render URL For Model
VITE_MODEL_URL='your_model_hostname'

# Firebase Authentication Keys
VITE_FIREBASE_API_KEY=your-api-key
VITE_FIREBASE_AUTH_DOMAIN=your-auth-domain
VITE_FIREBASE_PROJECT_ID=your-project-id
VITE_FIREBASE_STORAGE_BUCKET=your-storage-bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your-messaging-sender-id
VITE_FIREBASE_APP_ID=your-app-id
VITE_FIREBASE_MEASUREMENT_ID=your-measurement-id

```

For detailed instructions on obtaining these values, refer to the [EnvVarSetUpGuideline.md](.github/EnvVarSetUpGuideline.md) file.
<h3 align="right"><a href="#top">⬆️</a></h3>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🖥️ Key Features Implementation</h2>

### 1. User Authentication
- User registration and login
- Password reset functionality
- Profile management
- Role-based access control (patient/doctor)

### 2. Video Consultation
- Real-time video calls using Jitsi
- Appointment scheduling and management
- Doctor availability calendar

### 3. Medical Records Management
- Patient history viewing
- Prescription generation and downloading
- Health records storage and retrieval

### 4. Payment Integration
- Wallet system using Stripe
- Payment history tracking
- Secure payment processing

### 5. Medicine Marketplace
- Browse and search medicines
- Shopping cart functionality
- Order tracking
- Review and rating system

### 6. Disease Prediction
- Symptom-based disease prediction
- Health recommendations

### 7. UI/UX Features
- Responsive design for all devices
- Dark/Light mode toggle
- Accessibility features
- Intuitive navigation

<h2>⚡Project Admin and Collaborators</h2>

<table>
<tr>
<td align="center">
<a href="https://github.com/PratikMane0112"><img src="https://avatars.githubusercontent.com/u/153143167?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Pratik Mane <br> (Project Admin)</b></sub>
</td>
<td align="center">
<a href="https://github.com/HarshwardhanPatil07"><img src="https://avatars.githubusercontent.com/u/126240589?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Harshwardhan Patil <br> (KWoC Mentor) </b></sub>
</td>
<td align="center">
<a href="https://github.com/AdityaBavadekar"><img src="https://avatars.githubusercontent.com/u/64344960?v=4" height="140px" width="140px" alt="Pratik Mane"></a><br><sub><b>Aditya Bavadekar <br> (SWoC Mentor)</b></sub>
</td>
<td align="center">
<a href="https://github.com/RajKhanke"><img src="https://avatars.githubusercontent.com/u/137288727?v=4" height="140px" width="140px" alt="Raj Khanke"></a><br><sub><b>Raj Khanke <br> (DWoC Mentor) </b></sub>
</td>

</tr>
</table>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🫂Project Contributors</h2>

<a href="https://github.com/PratikMane0112/TelMedSphere/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=PratikMane0112/TelMedSphere&cache_burst=1" />
</a>

<h2><a href="https://discord.gg/qsdDRKak28">Join Discord Server↗️</a></h2>

<!-- --------------------------------------------------------------------------------------------------------------------------------------------------------- -->

<h2>🧾License</h2>

This project is licensed under the Apache License 2.0. See the [LICENSE](https://github.com/PratikMane0112/TelMedSphere/blob/master/LICENSE) file for more details.
  
```
 Copyright 2025 Pratik Mane

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
```

<h3 align="center">
  <a href="#top">⬆️ Back to top</a>
</h3>

