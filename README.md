# JAMB FreeHub 2026 🎓
Welcome to the ultimate, 100% free, offline-first Progressive Web App (PWA) dedicated to helping students prepare for the 2026 JAMB UTME in **English**, **Literature**, **Government**, and **CRS**.
## Features
- **PWA & Offline First**: Works completely offline after the first visit. Add it to your home screen!
- **Syllabus & Notes**: Full coverage of the 2026 JAMB Syllabus, including detailed notes on all required Literature texts and literary devices.
- **Practice Mode**: Topic-by-topic practice with immediate feedback and comprehensive explanations.
- **Realistic CBT Mock**: A faithful recreation of the JAMB CBT interface. Features a live timer, intuitive navigation sidebar, official on-screen calculator, keyboard shortcuts, and detailed performance breakdown at the end.
- **Responsive & Dark Mode**: Perfect on phones, tablets, and desktops. Easy on the eyes for late-night study sessions.
- **Local Storage**: All your mock scores and progress are saved securely on your device.
## Adding More Questions
Adding new content is incredibly simple. You don't need any backend or database! All questions and syllabus data are stored in pure JSON format inside the source code.
1. Open `src/data/questions.ts`.
2. Add new question objects to the generator function or direct array following this structure:
   \`\`\`json
   {
     "id": "eng_100",
     "subject": "English",
     "topic": "Comprehension",
     "question": "Your question text here...",
     "options": { "A": "...", "B": "...", "C": "...", "D": "..." },
     "answer": "B",
     "explanation": "Detailed explanation here..."
   }
   \`\`\`
3. Save the file. The app will automatically include them!
To add new subjects, simply update the arrays in `src/pages/HomePage.tsx`, `CBTMode.tsx`, and `ReadingMode.tsx` to include your new subject name, and append the syllabus JSON in `src/data/syllabus.ts`.
## Deployment Instructions (Free in 2 Minutes)
You can host this entire app for completely free on services like **Vercel**, **Netlify**, or **GitHub Pages**.
### Vercel / Netlify
1. Create a free account on [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/).
2. Connect your GitHub repository containing this code.
3. Select the repository and set the framework preset to **Vite** (or ensure the build command is `npm run build` and output directory is `dist`).
4. Click **Deploy**. Your JAMB CBT app will be live and ready for millions of students!
### GitHub Pages
1. Push this repository to GitHub.
2. Go to your repository settings -> **Pages**.
3. Under **Source**, choose **GitHub Actions**.
4. Use the default static HTML or Node.js workflow to build and deploy the `dist` folder.
5. (Because we used `HashRouter`, routing works perfectly out of the box with zero 404 errors!)
## UI Screenshot Descriptions
- **Home Dashboard**: Features a vibrant blue header, interactive progress tracking cards, and quick-action buttons to enter different modes.
- **Reading Mode**: A two-column layout on desktop (collapsible sidebar on mobile) letting students browse topics via smooth accordion menus, beautifully formatted for reading.
- **Practice Mode**: A clean, distraction-free interface where clicking an option immediately reveals the answer, color-coded green for correct and red for incorrect, followed by an in-depth explanation box.
- **CBT Interface**: A highly realistic JAMB mock screen. A green top bar displays the timer and candidate details. The left sidebar contains a grid of question numbers (color-coded when answered). The main area presents the question clearly with large clickable options, and a draggable functional calculator modal can be opened at any time.
---
_Built for the success of 2026 UTME candidates. 100% Free Forever._
