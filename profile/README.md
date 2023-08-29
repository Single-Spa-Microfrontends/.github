# Microfrontend Architecture (MFA) with single-spa

## Introduction

Microfrontends (MF) break up a monolithic frontend app into smaller, more manageable pieces. These pieces can then be developed, tested, and deployed independently, potentially by different teams. The single-spa library facilitates this architecture, acting as a root configuration (or "orchestrator") to manage these micro-apps.

The aim of our project under the `Single-Spa-Microfrontends` organization is to showcase this architecture, integrating multiple frontend frameworks and a shared style guide.

## Components

1. **Root-config**: Acts as the central hub for the microfrontends. It initializes and loads micro-apps based on route or other conditions.
   - **Running Port**: 9000
   - **Responsibility**: Orchestrates the loading of micro-apps.

2. **React Navbar**: A microfrontend built with React, responsible for the navigation bar.
   - **Running Port**: 9001

3. **Angular Legacy (v11)**: An older version of the app built using Angular v11.
   - **Running Port**: 9002
   - **Notes**: Must use node v16 and @angular/cli@11.

4. **Angular New App (v16)**: A newer, revamped version of the app, built using Angular v16.
   - **Running Port**: 9003

5. **Styleguide**: Houses shared components and styles. Uses TailwindCSS to maintain a consistent look and feel across micro-apps.
   - **Running Port**: 9004 (or subsequent)
   - **Features**: With TailwindCSS's purge feature, we can prevent CSS bloating by removing unused styles, reducing the bundle size significantly.

## How to Run

### Prerequisites

- Git, to clone the repositories.
- Node.js. 
  - For Angular v11 (Legacy): Node v16
  - For all other repositories: Node v18

### Setup

1. Navigate to our organization's [repository page](https://github.com/orgs/Single-Spa-Microfrontends/repositories) and clone all repositories to your local machine.
   
2. Open a separate terminal window or tab for each cloned repository.

3. For each repository:
   1. Navigate to the repo's root directory.
   2. Install the necessary dependencies:

4. For the Angular v11 legacy app, ensure you're using Node v16 and install the specific Angular CLI version:
   ```
   npm install -g @angular/cli@11
   ```

5. Start each application by running the appropriate npm script.

   ```
   pnpm start
   ```

   Angular Legacy

   ```
   yarn start
   ```
## Future Endeavors

Our team aims to continually refine this project and showcase even more advanced functionalities and integrations. We're also working towards deploying this setup on GCP for a live proof-of-concept. Feedback, contributions, and suggestions are always welcome!

---

**Note**: Microfrontends provide a scalable architecture, especially for large projects or teams. It facilitates independent development, testing, and deployment, making the development lifecycle more efficient. We hope our initiative showcases its potential and encourages its adoption.

---

![high_level_architecture.drawio.svg](https://github.com/Single-Spa-Microfrontends/.github/blob/main/high_level_architecture.drawio.svg)
![high_level_micro_apps_updates.drawio.svg](https://raw.githubusercontent.com/Single-Spa-Microfrontends/.github/main/micrfrontend-update-representation.drawio.svg)
