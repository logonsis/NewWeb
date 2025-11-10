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

## Coding Standards and Best Practices

*   **File Naming:**
    *   React components should use `PascalCase` (e.g., `UserProfile.tsx`).
    *   Utility files, hooks, and other non-component files should use `kebab-case` (e.g., `use-auth.ts`, `api-client.ts`).
    *   Directory names must be all lower-case (e.g., `src/pages`, `src/components`).
*   **Component Design:**
    *   Aim for small, focused components with a single responsibility.
    *   Create a new file for every new component or hook, no matter how small. Avoid adding new components to existing files.
    *   Components should generally be 100 lines of code or less. Refactor larger components into smaller, more manageable pieces.
*   **Responsiveness:** All UI designs must be inherently responsive, adapting gracefully to various screen sizes using Tailwind CSS utilities.
*   **Error Handling:** Utilize toast notifications for user-facing feedback on important events (success, error, loading). Avoid `try/catch` blocks unless explicitly requested, allowing errors to propagate for centralized debugging.
*   **Code Readability and Maintainability:**
    *   Write clear, concise, and self-documenting code.
    *   Follow consistent formatting and linting rules.
    *   Prioritize simplicity and elegance over overly complex solutions.
*   **Completeness:** All implemented features must be fully functional with complete code. Avoid placeholders, partial implementations, or `TODO` comments for features that are part of a user request.