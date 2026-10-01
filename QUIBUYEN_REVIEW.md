# Peer Project Review: MediConsult (CSIT321)

**Reviewer:** Quibuyen
**Project:** MediConsult, a telemedicine web platform built with ASP.NET Core Blazor (Interactive Server) and Tailwind CSS
**Author (per commit history):** renzo1417

---

## Project Structure Rating: 9 / 10

The repository is well organized and easy to navigate. Everything under `Components/` is grouped by role: `Layout/` (Navbar, Footer, MainLayout), `Pages/` (Home, Login, Signup, HowItWorks, Reviews, Error), `Sections/` (the landing-page sections such as Hero, Services, Pricing and About Us) and `Common/` (the shared `AppLogo`). Static files are separated into `wwwroot/css`, `wwwroot/js` and `wwwroot/images`. The page files stay short because the landing page is built from section components. For example, `Home.razor` is only 21 lines and composes the sections, and the logo is a reusable component rather than copy-pasted markup. File and folder names are descriptive and consistently PascalCase, so I could find any part of the UI without searching.

The repository is also clean and well documented. `.gitignore` is the standard .NET one, `bin/` and `obj/` are not tracked (a commit even says it untracked build artifacts), and the project includes `.vscode/launch.json` and `tasks.json` for running and debugging. The detailed `README.md` explains what the project is, its features, routes, design system (fonts and colour palette) and how to run it. This is something many repos lack. The commit history is linear, and the messages consistently use Conventional Commits with scopes, for example `feat(reviews): add patient reviews page with 3D coverflow and rating form` and `chore(git): add .gitignore and untrack build artifacts`.
---

## Front-End Rating: 10 / 10

The interface is polished, modern and consistent. The design is a clean white base with a deep charcoal (`brand-dark`) and a lime accent (`brand-lime`), set in Space Grotesk. The same pill-shaped buttons, rounded cards, spacing and hover behaviour are used on every page, so the whole site feels like one product. Hierarchy is clear, with large bold headlines (the hero highlights "expert care," in a lime chip), muted supporting text and obvious primary and secondary calls to action ("Book a Consultation" and "How it works"). The sticky, blurred navbar has animated underline hover states and gives access to every section and page, including Home, About Us, Services, How It Works, Pricing, Reviews, Login and Sign Up. The `/#section` links scroll to the correct landing-page section.

The standout features are the interactive ones. The `/how-it-works` page is a full-screen simulated clinical portal in a device frame that lets the user step through all six stages of care: symptom assessment, doctor matching, booking, live consultation, digital prescription and follow-up. The `/reviews` page has a 3D coverflow carousel of patient testimonials and a review form with a hover star rating, a live score label, service selection, validation messages and a success state. The landing page adds scroll-triggered reveal animations, button hover motion with a custom spring curve (`motion.js` and the `motion-btn` classes) and a scroll progress indicator, and these effects add polish without getting in the way. The Login and Signup pages use a clean two-column layout with an image panel, a back link, a show/hide password control and cross-links between them.

The layout is responsive. The pages use `md:` and `lg:` breakpoints throughout, the 12-column hero grid stacks on small screens, and the navbar collapses into a hamburger menu with a mobile dropdown and an `aria-label` on its toggle button. Text is large and high-contrast (dark text on white), so it is very readable. Overall this is a complete, visually impressive and easy-to-use front end.
