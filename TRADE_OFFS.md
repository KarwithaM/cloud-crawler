# Architectural Trade-offs & Engineering Decisions

In the spirit of rapid prototyping, I made specific architectural choices to maximise the "Vibe" and User Experience within the hackathon timeframe. Here is the engineering rationale behind my decisions.

### 1. Client-Side SVG Animations vs. Heavy WebGL/3D
- **The Choice:** I built the Wizard Tutor using modular, state-driven SVG groups animated via Framer Motion, rather than a heavy 3D engine.
- **The Trade-off:** I sacrifice photorealistic 3D graphics for **instant load times, zero external asset dependencies, and perfect scalability** across all devices. The "paper-doll" modular approach allows the AI to easily generate new animations (like pulling a lever) by just rotating an SVG `<g>` tag.

### 2. Supabase Postgres vs. LocalStorage Only
- **The Choice:** While the score is cached in `localStorage` for instant UI updates, the actual questions are fetched live from a Supabase PostgreSQL database.
- **The Trade-off:** This adds a network request on initial load (requiring a "Summoning" loading state), but it proves **full-stack capability**, allows for future features like global leaderboards, and separates the data layer from the presentation layer. I secured the data using Supabase Row Level Security (RLS).

### 3. "Honest Quizzing" Penalty System vs. Standard Quiz
- **The Choice:** Users lose -0.5 points for a wrong answer and gain +1 for a correct answer. 
- **The Trade-off:** This might frustrate users who just want to click through quickly. However, from a **Learning Value** perspective, it mathematically prevents "brute-forcing" (clicking all 4 options until one turns green). It forces the user to read the "Lore Unlocked" explanation, genuinely improving exam readiness.

### 4. Mock Data Fallback for AI Generation (Custom Forge)
- **The Choice:** If the AI URL-ingestion feature fails to scrape a protected URL (like a private Google Doc), the backend returns a pre-verified mock array.
- **The Trade-off:** The user gets generic questions instead of AI-generated ones. However, this guarantees **100% uptime for the demo**, ensuring the app never crashes in front of a judge due to third-party API rate limits or CORS scraping blocks.
