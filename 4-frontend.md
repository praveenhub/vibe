Untitled-1                                   frontend_guidelines_document.mdc U X
.cursor > rules > frontend_guidelines_document.mdc

Rule Type
Always                       This rule attached to every chat and command+k request

Update this rule if user requested changes to the project requirement, etc.
# Braindump Frontend Guideline Document

This document describes the frontend architecture, design principles, styling and theming, component structure, state
management, routing, performance optimization, and testing practices for the Braindump application. The goal is to ensure
our frontend setup is scalable, maintainable, and provides an exceptional user experience for users using our AI-powered
journaling and productivity web application.

## 1. Frontend Architecture

Our frontend is built using a modern stack designed for performance and simplicity. We use **Next.js** as our primary
framework, allowing server-side rendering and static site generation when beneficial for performance. The project
leverages **Typescript** for type safety and early error detection, and **Tailwind CSS** combined with **Shadcn UI** for
customizable, component-driven design. This architecture is built on a component-based paradigm, meaning that UI elements
are reusable and encapsulated, which supports easier maintenance and scalability as the project grows.

Key libraries and integrations:

*   Next.js: Enables advanced routing, SSR/SSG, and improved SEO.
*   Typescript: Provides clarity and consistency across components.
*   Tailwind CSS: Enables rapid styling using utility classes, ensuring responsive design and consistency.
*   Shadcn UI: Helps build sophisticated UI components with a subtle and modern design language.

This approach keeps our codebase modular and promotes a clear separation of concerns, making it easier to update
individual components without affecting the overall application.

## 2. Design Principles

Our design is guided by a few core principles:

*   **Usability:** The user experience is made simple and intuitive. Every interface element is designed with the user in
    mind, ensuring ease of use.
*   **Accessibility:** Our application is built to be inclusive. We ensure that text is clear, navigation is easy, and
    components are accessible to all users.
*   **Responsiveness:** The design automatically adapts to different devices and screen sizes, ensuring a consistent
    experience whether on a desktop, tablet, or mobile phone.
*   **Calm and Clarity:** Reflecting our core values, the visual language is soothing and uncluttered, making use of
    colors like light blue, green, and lavender, paired with modern sans-serif fonts for a professional look.

These principles are reflected throughout our UI, ensuring that layouts, interactions, and animations serve usability and
visual harmony.

## 3. Styling and Theming

Our styling approach uses the power of Tailwind CSS, which prioritizes utility classes to build designs quickly and
consistently. We also follow some aspects of BEM (Block Element Modifier) for our custom CSS classes where necessary,
ensuring maintainability and clear class definitions.

### Theming

To maintain a consistent look, we adhere to a calming, modern design aesthetic with the following details:

*   **Style:** Clean, modern design with subtle cues of glassmorphism and flat/MATERIAL touches, accentuating clarity and
    calm.
*   **Color Palette:**
    *   Primary: Light blue (#ADD8E6)
    *   Secondary: Soft green (#90EE90)
    *   Accent: Lavender (#E6E6FA)
    *   Neutrals: Variants of white, gray, and black for text and backgrounds.
*   **Fonts:** Modern sans-serif fonts such as Helvetica, Arial, or similar web-safe fonts to maintain the clean design
    without distraction.

Using Tailwind ensures we have both rapid prototyping facilities and full customization when needed. The theming system
makes sure that any future changes to the palette or design elements can be easily applied across the whole application.

## 4. Component Structure

The Braindump frontend is organized in a modular, component-based architecture. Components are isolated pieces of UI that
can be reused across the application, leading to less redundancy and making the code more manageable over time.

Key aspects:

*   **Folder Structure:** Components are organized according to functionality. For example, interactive components like
    Voice-to-Text Journaling, manual editing areas, and timers for Focus Mode are kept in a dedicated components folder.
*   **Reusability:** Using Shadcn UI and custom components, common UI patterns (buttons, forms, cards, dialogues) are
    reused everywhere.
*   **Isolation:** Each component encapsulates its styling and logic, making debugging easier and promoting independent
    development of UI parts.

Component examples include:

*   Journaling input section (supports text and voice input).
*   AI-generated insights and actionable to-dos display elements.
*   Focus Mode and timer components.
*   Navigation and report display components.

## 5. State Management

For managing the state across the application, we use a combination of React Context API and local component state
management. For more complex, cross-component communication, a structured pattern ensuring that data such as user
entries, AI insights, and session details remain synchronized across views is used.

Key highlights:

*   **React Context API:** Provides a global state accessible to multiple components without prop-drilling.
*   **Local State:** Utilized within individual components for most user interactions.
*   **Synchronization:** Ensures that changes to journaling entries, to-dos, or settings (like Focus Mode timers) are
    reflected immediately in the user interface.

This strategy guarantees a seamless and responsive interaction model throughout the application.

## 6. Routing and Navigation

Routing in Braindump is managed by Next.js' built-in file-based routing system. This makes defining routes as simple as
creating files or directories in our pages folder.

Features include:

*   **Dynamic Routing:** Supports both static routes (e.g., daily summaries, weekly reports) and dynamic routes (e.g.,
    individual journal entry pages).
*   **Navigation Structure:** The UI includes a consistent navigation bar and sidebar, offering quick access to key
    sections such as journaling, to-dos, focus mode, and reports.
*   **Integration with Auth:** The authentication state, using Clerk, influences accessible regions of the app. Users who
    are not signed in are guided to the sign-in page, ensuring secure access.

This simplicity in routing ensures that users can easily move between different parts of the application without confusion.

## 7. Performance Optimization

To keep the application fast and responsive, we incorporate several performance best practices:

*   **Code Splitting & Lazy Loading:** Components that are not immediately necessary are loaded on demand. This reduces
    the initial bundle size and speeds up page loads.
*   **Asset Optimization:** Images and assets are optimized using Next.js built-in image optimization, ensuring that
    every image is responsive and efficiently loaded.
*   **Selective Transpilation:** Only necessary polyfills and libraries are loaded, keeping the overall code footprint
    minimal.
*   **Caching Strategies:** Leveraging caching both on the server and client assures smoother transitions especially when
    dealing with APIs (Deepgram, OpenAI) and third-party integrations.

These techniques combine to create a smooth user experience, even during heavier tasks like voice-to-text transcription
or loading detailed productivity reports.

## 8. Testing and Quality Assurance

To ensure our frontend code is reliable and bug-free, Braindump employs a thorough testing approach:

*   **Unit Testing:** Each component is tested individually to verify that it works as expected. Tools like Jest and
    React Testing Library are used.
*   **Integration Testing:** Combined behavior of multiple components is tested to ensure they interact correctly. This
    ensures end-to-end workflows function properly.
*   **End-to-End Testing:** Real user flows, such as signing in, making a journal entry using voice input, and generating
    AI insights, are simulated using tools like Cypress.
*   **Linting and Style Checks:** Consistent code style is maintained using ESLint and Prettier, which run as part of our
    CI pipeline.

These testing strategies help maintain high quality as new features are added and modifications are made.

## 9. Conclusion and Overall Frontend Summary

In summation, the Braindump frontend is designed to be a modern, responsive, and accessible web application aligned with
the project's goal of providing clear insights and actionable productivity steps. The use of Next.js, Typescript,
Tailwind CSS, and Shadcn UI, combined with well-defined component structures and state management, ensures that the
application remains scalable and maintainable. Our emphasis on clean design (calm tones, modern sans-serif fonts),
performance optimizations, and thorough testing sets us apart, providing users with a robust and delightful experience.

This comprehensive guideline outlines how every part of our frontend aligns with Braindump's mission: to turn raw
thoughts into clear, actionable insights while ensuring an intuitive and engaging user experience.
