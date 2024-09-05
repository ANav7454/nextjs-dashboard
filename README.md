# Creating a new project

    ```bash
    npm install -g pnpm

    npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm
    ```

# Running the development server

Install the project's packages 

  pnpm i 

  pnpm run dev
    Starts the development server.

  pnpm run build
    Builds the app for production.

  pnpm start
    Runs the built app in production mode.


# Steps

## CSS & Fonts
* Add global css into the top-level component "app/layout.tsx"
* Add fonts "app/ui/fonts.ts" and add fonts to "app/layout.tsx"
    * Is possible add secondary fonts.ts , see "app/page.tsx" visit https://fonts.google.com/

## Images optimization
* Add static images in to /public folder. 
  * Files inside /public can be referenced in your application.
* Use **Image** component 
  ```ts
    import Image from 'next/image';
  ```
  ```html
    <img
    src="/hero.png"
    alt="Screenshots of the dashboard project showing desktop version"
/>
    ```
 ## Layouts and Pages

### Pages
 **Routing:**
  Next.js uses file-system routing where folders are used to create nested routes.

  **¡Each folder represents a route segment that maps to a URL segment!!**

    ex: /app/dashboard/page.tsx is associated with the /dashboard path (Importanta: nextjs expect a page.tsx file name)

### Creating the dashboard layout

  Dashboards have some sort of navigation that is shared across multiple pages. In Next.js, you can use a special layout.tsx file to create UI that is shared between multiple pages. 

    see /app/dashboard/layout.tsx  
    (Important: nextjs expect a layout.tsx file name)

  First, you're importing the **SideNav** component into your layout. Any components you import into this file will be part of the layout.

  The **Layout** component receives a children prop. This child can either be a page or another layout. In your case, **the pages inside /dashboard will automatically be nested inside a Layout**

## Navigating Between Pages

The **Link** component , see app/ui/dashboard/nav-links.tsx

To showing active links Next.js provides a hook called **usePathname()** that we can use to check the path and implement this pattern.

  see /app/ui/dashboard/nav-links.tsx





