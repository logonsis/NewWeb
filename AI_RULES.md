# AI Development Rules

This document outlines the technical stack and specific library usage guidelines for developing this application. Adhering to these rules ensures consistency, maintainability, and efficient development.

## Tech Stack Overview

*   **Framework:** React
*   **Language:** TypeScript
*   **Routing:** React Router (routes defined in `src/App.tsx`)
*   **Styling:** Tailwind CSS
*   **UI Components:** shadcn/ui (built on Radix UI)
*   **Icons:** lucide-react
*   **Project Structure:**
    *   All source code resides in the `src` directory.
    *   Pages are located in `src/pages/`.
    *   Components are located in `src/components/`.
    *   The main entry page is `src/pages/Index.tsx`.
*   **Responsiveness:** All designs must be responsive.
*   **Error Handling:** Use toast components for user feedback on important events. Avoid `try/catch` blocks unless specifically requested, allowing errors to bubble up for better debugging.

## Library Usage Guidelines

*   **React:** Use as the primary library for building user interfaces.
*   **TypeScript:** Mandatory for all new and modified code to ensure type safety and improve code quality.
*   **React Router:** Exclusively for client-side navigation. All top-level routes should be defined within `src/App.tsx`.
*   **Tailwind CSS:** The sole framework for all styling. Utilize its utility classes for layout, spacing, colors, typography, and responsive design. Avoid custom CSS files unless absolutely necessary for very specific, complex cases not covered by Tailwind.
*   **shadcn/ui:** Leverage these pre-built, accessible components for common UI elements (e.g., buttons, forms, dialogs). **Do not modify the original `shadcn/ui` component files.** If customization is needed, create a new component that wraps or extends the `shadcn/ui` component.
*   **Radix UI:** This library provides the unstyled, accessible primitives that `shadcn/ui` is built upon. While `shadcn/ui` is preferred for styled components, Radix UI can be used directly for more advanced, custom accessible components if `shadcn/ui` doesn't offer a suitable option.
*   **lucide-react:** Use this library for all icons throughout the application.