# Juhi Jain · Portfolio

**Live site → [juhijain06.github.io](https://juhijain06.github.io)**

My personal portfolio website. I'm a B.Tech CSE (AI, ML & Robotics) graduate and a full-stack engineer. I build frontends with HTML, CSS and JavaScript, and the APIs and databases behind them with C#, ASP.NET Core and SQL Server.

The site is a single hand-written HTML file. It has no frameworks, libraries or build step.

---

## ✨ What makes it different

### 1. Query my résumé in SQL
The terminal at the top of the site is real. My résumé is stored as tables, and visitors can run SQL against it right in the browser:

```sql
SELECT name, year FROM projects ORDER BY year DESC;
SELECT COUNT(*) FROM skills WHERE category = 'AI/ML';
SELECT title FROM certifications WHERE title LIKE '%AI%';
```

- **Tables:** `projects`, `experience`, `skills`, `education`, `certifications` (type `tables` to see their columns)
- **Supported SQL:** `SELECT` with column lists or `*`, `COUNT(*)`, `WHERE` (`=`, `!=`, `<>`, `>`, `<`, `>=`, `<=`, `LIKE`, `AND`), `ORDER BY … ASC|DESC`, `TOP n` / `LIMIT n`
- Errors are styled like SQL Server's, for example `Invalid column name 'salary'`
- **Shell commands:** `help`, `whoami`, `about`, `projects`, `experience`, `skills`, `education`, `contact`, `tables`, `theme`, `api`, `clear`, plus ↑/↓ for command history
- Easter eggs: try `DROP TABLE projects` or `sudo hire juhi` 😉

The SQL engine is about 40 lines of vanilla JavaScript. A regular expression parses the query into its clauses, and the engine then filters, sorts, limits and projects plain JavaScript arrays of objects.

### 2. View the site as an API response
The **`{ }`** button in the nav bar renders the whole portfolio as a `GET /api/v1/juhi-jain → 200 OK` JSON response, syntax-highlighted.

### 3. Other details
- Light and dark themes (follows your system setting and remembers your choice)
- Fully responsive, from phone to desktop
- Scroll-reveal animations that respect `prefers-reduced-motion`
- Accessible labels and keyboard-friendly terminal

---

## 🛠️ Tech stack

| Layer | Used |
|---|---|
| Structure | HTML5 (semantic sections) |
| Styling | CSS3: Grid, Flexbox, custom properties for theming, media queries |
| Behaviour | Vanilla JavaScript (ES6+): DOM, events, IntersectionObserver, localStorage |
| Fonts | Google Fonts: Fraunces, Inter, JetBrains Mono |
| Hosting | GitHub Pages |

---

## 📁 Project structure

```
.
├── index.html    # the entire site: markup, styles and scripts
├── README.md
└── .gitignore
```

---

## 🚀 Run it locally

There's nothing to install. Either open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 5173
```

Then visit <http://localhost:5173>.

## 🔄 Deploying updates

The site deploys automatically with GitHub Pages from the `main` branch:

```bash
git add .
git commit -m "Describe the change"
git push
```

The live site updates within a minute or two.

---

## 📬 Contact

- **LinkedIn:** [juhi-jain-a9ab67248](https://linkedin.com/in/juhi-jain-a9ab67248)
- **GitHub:** [@JuhiJain06](https://github.com/JuhiJain06)
- **Email:** juhijain0604@gmail.com

Other projects: [MovieApi](https://github.com/JuhiJain06/MovieApi) (ASP.NET Core backend) · [RePlastix](https://github.com/JuhiJain06/RePlastix-Innovations-Transforming-Plastic-Waste-into-Sustainable-Solutions) (Salesforce platform)

---

© 2026 Juhi Jain
