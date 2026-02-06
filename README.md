# 🧪 Dong Group Website @ HKU

This is the academic website for **Professor Renhao Dong's research group** at **The University of Hong Kong (HKU)**.  
It is designed for clarity, maintainability, and scalable content management.

---

## 📐 Architecture Overview

The website follows a **content-layout separation** and **configuration-driven** structure:

```
/
├── config/                # Global configs: navigation, image assets, etc.
├── content/               # Page-specific content (text, data)
├── components/            # Pure rendering components (no hardcoded content)
├── pages/                 # Top-level routes and layout assembly
├── public/assets/images/  # Static images referenced across the site
└── README.md              # This file
```

---

## 🌐 Tech Stack

- **Framework:** React + TypeScript
- **Styling:** Tailwind CSS
- **Content-Driven:** All content stored in `.ts` files, structured for editors and devs
- **Hosting:** GitHub Pages / Vercel / Netlify (choose one)
- **Design Tool:** [Figma Make](https://www.figma.com)

---

## 📦 Installation & Local Development

```bash
git clone https://github.com/your-username/groupwebsite.git
cd groupwebsite

# Install dependencies
npm install

# Start local server
npm run dev
```

Open `http://localhost:3000` in your browser.

---

## ✍️ Content Editing Guide

All website content (people, news, publications, facilities, etc.) lives in the `/content` folder.

- **Publications:** `content/publicationContent.ts`
- **News & Activities:** `content/newsContent.ts`
- **Team:** `content/teamContent.ts`
- **About Us:** `content/aboutUsContent.ts`

Use TypeScript-friendly structure to ensure consistency. All content is hot-reloadable.

---

## 🖼️ Image Management

All image URLs are referenced from a central config file:

```
config/imageAssets.ts
```

Organized by category:

```ts
export const imageAssets = {
  team: {
    postdocs: {
      liZheng: 'https://raw.githubusercontent.com/...',
    },
  },
  facilities: {
    synthesisLab: 'https://raw.githubusercontent.com/...',
  },
};
```

🟡 Store all group images in:  
`/public/assets/images/`

Upload images via Git and reference them using **raw GitHub URLs**.

---

## ✏️ How to Add a New Team Member

1. Upload image to `public/assets/images/`
2. Add image URL to `config/imageAssets.ts`
3. Add team member to `content/teamContent.ts`

---

## 📚 Publications Format

Publications are grouped by year. Each entry includes:

- Title
- Authors (with formatting)
- Journal
- DOI

```ts
{
  year: 2024,
  entries: [
    {
      title: '...',
      authors: 'Dong R.*, Wang J.+, ...',
      journal: 'Nature Materials',
      doi: 'https://doi.org/...',
    },
  ],
}
```

---

## 📰 News & Activities

Only events from the **past 3 years (2023–2025)** are displayed.  
Each event links to a detailed news item via ID or slug.

---

## 🌈 Theme & Colors

Color scheme: **Sky Blue + Amber Yellow**

- Primary: `#3F8CFF`
- Secondary: `#FFC94D`
- Background: `#F3F8FF`
- Text: `#0B1B33`

Adjustable via Tailwind config or global CSS variables.

---

## ✅ To Do / Milestones

- [x] Project scaffolding complete
- [x] Figma prototype synced
- [ ] Image assets uploaded
- [ ] Publications, patents, and team filled
- [ ] Deploy to production

---

## 🧠 Maintainers

- Frontend & Content: [Your Name]
- PI: Prof. Renhao Dong, HKU

---

## 📄 License

MIT License
