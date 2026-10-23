# Cloud Crawler: Crawl Your Way to Cloud Mastery

> **Disclaimer:** *Cloud Crawler is an unofficial, community-built study tool created for the #1MillionDevs Vibe Coding Hackathon. It is not affiliated with, endorsed by, or sponsored by Microsoft. All AZ-900 concepts are based on the public Microsoft Learn skills outline. No real exam questions or Microsoft logos are used.*

## The Quest
Azure AZ-900 prep is usually a chore of dry PDFs and boring flashcards. **Cloud Crawler** transforms exam prep into an interactive, gamified RPG. Guided by an animated Wizard Tutor, learners "crawl" through three realms of cloud concepts, battling questions to grow their soul orb and unlock ancient lore.

## Live Links
- **Play the Live Prototype:** [(https://cloud-crawler.lovable.app)]
- **Watch the Video Demo:**[(https://drive.google.com/file/d/1umGj2bn2hIVOdOOhjKSlxyly8vrrKmmU/view?usp=sharing)]
- **View the Pitch Deck:** [(https://drive.google.com/file/d/1eaGN0y6n6nnpG5kfQe_ljyok2vD-fKs9/view?usp=share_link)]

## Tech Stack & Architecture
Built rapidly using AI-assisted "Vibe Coding" tools with a focus on clean, scalable architecture:
- **Frontend & UI:** React, Tailwind CSS, Framer Motion (for modular, state-driven SVG Wizard animations).
- **Backend & Database:** Supabase (PostgreSQL) with Row Level Security (RLS) enabled for safe, live data fetching.
- **AI Prompt Engineering:** Utilized the **AIM (Actor, Input, Mission)** and **MAP (Memory, Assets, Prompt)** frameworks to generate complex, hallucination-free game logic and UI components via Lovable.dev.

## Core Features
1. **The Wizard Tutor:** A state-driven SVG character that reacts to gameplay (waves, reads scrolls, pulls levers, shakes her head), creating a highly engaging "vibe."
2. **Honest Quizzing Mechanics:** Gain +1 point for a first-try correct answer. Lose -0.5 points for a wrong guess. This mathematically prevents brute-forcing and rewards actual knowledge retention.
3. **Hybrid Lifeline:** A 9-block progress map tracks quest completion, while a glowing "Soul Orb" tracks fractional scores and shifts colors as the user levels up.
4. **Three Realms:** Questions are batched into *Concepts*, *Architecture*, and *Governance* to mirror the official AZ-900 skills outline.
5. **The Custom Forge (Scalability):** A unique feature allowing users to paste *any* public URL (e.g., a blog post or study guide). Our AI backend instantly scrapes the text and generates a custom, 9-question RPG realm, proving the tool scales beyond just AZ-900.
6. **Victory Scroll:** A post-game analytics screen showing first-try accuracy, weak realms, and a direct link to the official Microsoft practice assessment for continued learning.

## Local Development
```bash
# Clone the repo 
git clone https://github.com/KarwithaM/cloud-crawler.git
cd cloud-crawler

# Install dependencies
npm install

# Run the dev server
npm run dev
```
