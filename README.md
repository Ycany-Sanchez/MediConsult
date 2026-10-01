# MediConsult 🩺✨
> **Modern Virtual Healthcare & Teleconsultation Web Platform**  
> Built with **ASP.NET Core 8.0 Blazor Interactive Server** & **Tailwind CSS**.

---

## 📌 Project Overview
**MediConsult** is a modern telemedicine and digital healthcare web application designed to connect patients with board-certified healthcare professionals seamlessly. The platform streamlines patient-doctor interactions, from initial symptom intake and specialist matching to live consultations, digital prescriptions, and transparent care pricing.

This repository represents the frontend interface, clinical workflow simulator, and interactive user components built for our coursework project.

---

## 🚀 Key Features & Highlights

### 1. 🏠 Interactive Landing Page (`/`)
- **Hero Section**: High-impact medical headline with verified practitioner stats, trust badges, and direct call-to-actions.
- **About Us & Clinical Standards**: Clear presentation of medical accreditation, 24/7 availability metrics, and patient safety protocols.
- **Clinical Services**: Modular overview of primary care, teleconsultation, urgent care triage, and specialist referrals.
- **Workflow Preview**: Step-by-step breakdown of how care delivery works on the platform.
- **Transparent Pricing**: Transparent subscription and per-consultation pricing tiers with feature comparisons.
- **Live Testimonials Stage**: Interactive patient review cards with real-time modal submission flow.
- **CTA Banner & Footer**: Quick links, clinic contact info, and legal disclaimers.

### 2. 💻 Full-Screen Clinical Workflow Simulator (`/how-it-works`)
- An interactive, simulated doctor-patient portal rendered inside a responsive device frame.
- Allows reviewers to click through all **6 stages of care delivery**:
  1. **Symptom Assessment** — Intake questionnaire and triage.
  2. **Doctor Matching** — Instant AI matching with licensed specialists.
  3. **Schedule & Booking** — Calendar integration with appointment slots.
  4. **Live Virtual Consultation** — Video call interface with audio/video controls.
  5. **Digital Prescription** — Direct pharmacy dispatch and doctor's orders.
  6. **Care Follow-Up** — Progress tracking and post-care notes.

### 3. ⭐ Dedicated Reviews & Coverflow Showcase (`/reviews`)
- **3D Coverflow Carousel**: Interactive carousel to cycle through patient testimonials.
- **Category Filtering**: Filter reviews by rating and specialty (e.g., General Medicine, Pediatrics, Dermatology).
- **Interactive Review Submission**: Integrated modal form to submit ratings and feedback with live feedback validation.

### 4. 🔐 Authentication Portals (`/login`, `/signup`)
- Clean, accessible sign-in and registration interfaces.
- Patient and healthcare provider role-toggle views.
- Fully styled with responsive states, input focus treatments, and validation messaging.

---

## 🎨 Design System & Aesthetics
- **Typography**: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) for a clean, modern, and clinical aesthetic.
- **Color Palette**:
  - **Brand Lime (`#B4F435`)**: High-energy accent color for primary actions, badges, and highlights.
  - **Brand Dark (`#12161E`)**: Deep charcoal black for headers, dark cards, and premium contrast.
  - **Card Surface (`#161B24`)**: Elevated surface color for interactive containers.
  - **Clean Slate White**: Crisp white background for clinical clarity.
- **Interactions**:
  - Custom spring curves (`cubic-bezier(0.16, 1, 0.3, 1)`) for smooth button hovers.
  - Scroll-triggered reveal animations.
  - Real-time scroll progress indicator at the top of the viewport.

---

## 📂 Repository & Project Structure

The project follows a clean, modular Blazor component architecture:

```text
MediConsult/
├── Components/
│   ├── App.razor                      # Root HTML shell, Tailwind configuration & script imports
│   ├── Routes.razor                   # Blazor routing and route view definition
│   ├── _Imports.razor                 # Global namespace imports
│   ├── Common/                        # Reusable shared UI primitives
│   │   └── AppLogo.razor              # Brand logo with medical cross badge
│   ├── Layout/                        # Application layout shells
│   │   ├── Navbar.razor               # Navigation bar with responsive links & badges
│   │   ├── Footer.razor               # Footer layout with sitemap & accreditation
│   │   └── MainLayout.razor           # Default layout wrapper
│   ├── Pages/                         # Routable views (Pages)
│   │   ├── Home.razor                 # Landing page ("/")
│   │   ├── HowItWorks.razor           # Clinical workflow overview ("/how-it-works")
│   │   ├── Reviews.razor              # Testimonials & 3D coverflow showcase ("/reviews")
│   │   ├── Login.razor                # Patient & Doctor sign-in ("/login")
│   │   ├── Signup.razor               # Patient onboarding ("/signup")
│   │   └── Error.razor                # Error boundary view
│   └── Sections/                      # Self-contained section components
│       ├── HeroSection.razor          # Top hero banner & stats
│       ├── AboutUsSection.razor       # Company background & doctor network
│       ├── ServicesSection.razor      # Medical specialties & care offerings
│       ├── HowItWorksSection.razor    # Steps summary section
│       ├── HowItWorksInteractiveScreen.razor # 6-step interactive workflow simulator
│       ├── PricingSection.razor       # Subscription & consult price matrix
│       ├── StaggeredTestimonials.razor# Testimonial stage & inline review form
│       └── CtaBanner.razor            # High-conversion closing banner
├── Properties/
│   └── launchSettings.json            # ASP.NET Core server ports & launch profiles
├── wwwroot/                           # Static assets
│   ├── app.css                        # Global CSS utility extensions
│   ├── js/motion.js                   # Smooth reveal & UI micro-interactions
│   └── images/                        # Medical icons and preview assets
├── Program.cs                         # Server startup, Razor component registration
├── medconsult.csproj                  # .NET 8.0 SDK project configuration
└── README.md                          # Project documentation for reviewers
```

### Commit History Standard
All commits follow the [Conventional Commits](https://www.conventionalcommits.org/) convention (`feat:`, `fix:`, `refactor:`, `chore:`) to ensure clarity and chronological transparency.

---

## 🛠️ Tech Stack & Dependencies
- **Runtime & Framework**: [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) (`Microsoft.NET.Sdk.Web`)
- **Component Model**: Blazor Interactive Server Components
- **Styling**: Tailwind CSS (CDN configured with brand tokens) + Vanilla CSS
- **Icons**: Custom SVG Medical Icons & Lucide-inspired iconography
- **Fonts**: Space Grotesk via Google Fonts

---

## ⚙️ How to Run the Project Locally

### Prerequisites
- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) installed on your machine.
- A modern web browser (Chrome, Edge, Firefox, or Safari).

### Quick Start Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/renzo1417/MediConsult.git
   cd MediConsult
   ```

2. **Restore dependencies**:
   ```bash
   dotnet restore
   ```

3. **Run the development server**:
   ```bash
   dotnet run
   ```

4. **Access the application**:
   Open your browser and navigate to:
   - **HTTP**: `http://localhost:5025`
   - **HTTPS**: `https://localhost:7256`

*(Alternatively, use `dotnet watch` for hot-reload during code inspection).*

---

## 📋 Note for Peer Reviewers
When completing your evaluation, you can reference the project sections directly:
- **Project Structure**: Look into `Components/Sections`, `Components/Pages`, and `Components/Layout` to review component separation, naming consistency, and git commit history (`git log`).
- **Front-End**: Test the interactive pages (`/`, `/how-it-works`, `/reviews`, `/login`, `/signup`) to evaluate layout responsiveness, navigation usability, visual coherence, and typography.
