# Custom Dropdown Component

A custom dropdown component built with Svelte 5, TypeScript, and Tailwind CSS. This project demonstrates DOM manipulation, event handling, and creating responsive and interactive elements with JavaScript.

## 🎯 Project Overview

This is a solution for the [Custom Dropdown project](https://roadmap.sh/projects/custom-dropdown) from roadmap.sh. The dropdown component features:

- **Default State**: Shows placeholder text when no option is selected
- **Open State**: Reveals all available options when clicked
- **Selected State**: Displays the chosen item and highlights it
- **Responsive Design**: Built with Tailwind CSS for modern styling
- **TypeScript Support**: Fully typed for better development experience

## ✨ Features

- Custom dropdown implementation with HTML, CSS, and JavaScript
- Multiple dropdown instances with different states
- Hover effects and visual feedback
- Keyboard accessibility considerations
- Responsive design with Tailwind CSS
- TypeScript for type safety

## 🚀 Getting Started

### Prerequisites

- Node.js (version 18 or higher)
- Yarn package manager

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd RoadMap.sh-CustomDropdown
```

2. Install dependencies:
```bash
yarn install
```

### Development

Start the development server:

```bash
yarn dev
```

This will start the development server at `http://localhost:5173`. The app will automatically reload when you make changes to the code.

To open the app in a new browser tab automatically:

```bash
yarn dev -- --open
```

### Building for Production

To create a production build:

```bash
yarn build
```

To preview the production build:

```bash
yarn preview
```

## 🧪 Testing

Run the test suite:

```bash
# Run tests in watch mode
yarn test:unit

# Run tests once
yarn test
```

## 📝 Usage

The dropdown component accepts the following props:

- `options` (string[]): Array of options to display
- `status` (boolean): Whether the dropdown is open by default
- `defaultSelectedOption` (string): The initially selected option

### Example Usage

```svelte
<script lang="ts">
  import { Dropdown } from '$lib';
  
  let options = ['First Item', 'Second Item', 'Third Item', 'Fourth Item', 'Fifth Item'];
</script>

<!-- Basic dropdown -->
<Dropdown options={options} />

<!-- Dropdown with default open state -->
<Dropdown options={options} status={true} />

<!-- Dropdown with pre-selected option -->
<Dropdown options={options} status={true} defaultSelectedOption={options[2]} />

<!-- Dropdown with pre-selected option but closed by default -->
<Dropdown options={options} status={false} defaultSelectedOption={options[2]} />
```

## 🛠️ Available Scripts

- `yarn dev` - Start development server
- `yarn build` - Build for production
- `yarn preview` - Preview production build
- `yarn test` - Run tests
- `yarn test:unit` - Run tests in watch mode
- `yarn check` - Type check the project
- `yarn lint` - Lint the code
- `yarn format` - Format the code

## 🏗️ Tech Stack

- **Svelte 5** - Frontend framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Vite** - Build tool
- **Vitest** - Testing framework

## 📚 Project Structure

```
src/
├── lib/
│   ├── component/
│   │   └── dropdown.component.svelte  # Main dropdown component
│   └── index.ts                       # Component exports
├── routes/
│   └── +page.svelte                   # Demo page
└── app.html                           # HTML template
```

## 🔗 Related Links

- **Project Page**: [Custom Dropdown on roadmap.sh](https://roadmap.sh/projects/custom-dropdown)
- **Roadmap.sh**: [roadmap.sh](https://roadmap.sh) - Learn frontend development with interactive roadmaps

## 📄 License

This project is part of the roadmap.sh learning platform and is created for educational purposes.

---

**Note**: This is a solution for the Custom Dropdown project from [roadmap.sh](https://roadmap.sh/projects/custom-dropdown). The project helps developers practice DOM manipulation, event handling, and creating responsive and interactive elements with JavaScript.
