# Next.js + shadcn/ui — All Components Template

A ready-to-use Next.js template with **every shadcn/ui component pre-installed**. Built for developers who work in offline or restricted environments and can't run `npx shadcn add` on demand.

Clone it once, and you have the full shadcn/ui library at your fingertips — no internet required.

## Tech Stack

| Category          | Technology           | Version |
| ----------------- | -------------------- | ------- |
| Framework         | Next.js (App Router) | 16      |
| UI Library        | React                | 19      |
| Component Library | shadcn/ui            | 4       |
| Styling           | Tailwind CSS         | 4       |
| Language          | TypeScript           | 5       |
| Icons             | Lucide React         | 1.7     |
| Charts            | Recharts             | 3       |

## Getting Started

```bash
# Clone the repository
git clone https://github.com/waraiauyo/nextjs-shadcn-all-template.git
cd nextjs-shadcn-offline-template

# Install dependencies
npm install

# Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the result.

## Available Scripts

| Command         | Description              |
| --------------- | ------------------------ |
| `npm run dev`   | Start development server |
| `npm run build` | Build for production     |
| `npm run start` | Start production server  |
| `npm run lint`  | Run ESLint               |

## Included Components (55)

Every shadcn/ui component is pre-installed in `components/ui/`:

| Component       | Component      | Component     |
| --------------- | -------------- | ------------- |
| Accordion       | Alert          | Alert Dialog  |
| Aspect Ratio    | Avatar         | Badge         |
| Breadcrumb      | Button         | Button Group  |
| Calendar        | Card           | Carousel      |
| Chart           | Checkbox       | Collapsible   |
| Combobox        | Command        | Context Menu  |
| Dialog          | Direction      | Drawer        |
| Dropdown Menu   | Empty          | Field         |
| Hover Card      | Input          | Input Group   |
| Input OTP       | Item           | Kbd           |
| Label           | Menubar        | Native Select |
| Navigation Menu | Pagination     | Popover       |
| Progress        | Radio Group    | Resizable     |
| Scroll Area     | Select         | Separator     |
| Sheet           | Sidebar        | Skeleton      |
| Slider          | Sonner (Toast) | Spinner       |
| Switch          | Table          | Tabs          |
| Textarea        | Toggle         | Toggle Group  |
| Tooltip         |                |               |

## Included Dependencies

All required third-party libraries for shadcn/ui components are pre-installed:

- **radix-ui** / **@base-ui/react** — Accessible UI primitives
- **lucide-react** — Icon library
- **recharts** — Charting library (for Chart component)
- **embla-carousel-react** — Carousel engine
- **react-day-picker** / **date-fns** — Date picker & date utilities
- **react-resizable-panels** — Resizable panel layouts
- **cmdk** — Command menu (for Command component)
- **sonner** — Toast notifications
- **vaul** — Drawer component
- **input-otp** — OTP input fields
- **next-themes** — Dark/light theme support
- **class-variance-authority** / **clsx** / **tailwind-merge** — Styling utilities

## Project Structure

```
├── app/
│   ├── layout.tsx          # Root layout with Geist fonts
│   ├── page.tsx            # Home page
│   └── globals.css         # Global styles & theme tokens
├── components/
│   └── ui/                 # All 55 shadcn/ui components
├── hooks/
│   └── use-mobile.ts       # Mobile breakpoint detection hook
├── lib/
│   └── utils.ts            # cn() utility for class merging
└── components.json         # shadcn configuration
```

## Usage

Import any component directly:

```tsx
import { Button } from "@/components/ui/button";
import { Card, CardHeader, CardTitle, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";

export default function MyPage() {
    return (
        <Card>
            <CardHeader>
                <CardTitle>Login</CardTitle>
            </CardHeader>
            <CardContent className="flex flex-col gap-4">
                <Input placeholder="Email" />
                <Button>Submit</Button>
            </CardContent>
        </Card>
    );
}
```

## Customization

- **Theme** — Edit CSS variables in `app/globals.css` to customize colors, border radius, and spacing
- **Components** — All components live in `components/ui/` and can be modified directly
- **Fonts** — The template uses [Geist](https://vercel.com/font), configured in `app/layout.tsx`

## Why This Template?

Many workplaces restrict internet access for security reasons. Installing shadcn/ui components normally requires running `npx shadcn add <component>`, which fetches code from the internet. This template solves that problem by including everything upfront.
