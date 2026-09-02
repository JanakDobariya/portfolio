# Janak Dobariya — AI & ML Portfolio

Personal portfolio website for Janak Dobariya, an AI and machine-learning engineer pursuing a Master's in Computer Science with a focus on Natural Language Processing at Trier University.

**Live portfolio:** [janakdobariya.vercel.app](https://janakdobariya.vercel.app/)

The website is built with plain HTML, CSS, and JavaScript. It has no framework, package manager, database, or build step, so it is lightweight and easy to run locally.

## What is included

- Introduction and professional focus
- Education timeline
- AI, machine-learning, NLP, data-science, automation, and deployment skills
- Spoken languages
- Six featured projects on the homepage
- A separate ranked catalogue containing every published portfolio project
- GitHub and live-demo links for deployed applications
- Contact links for email, GitHub, and LinkedIn
- Responsive layouts for desktop, tablet, and mobile screens

## Project pages

- `index.html` is the main portfolio and contains the six strongest featured projects.
- `projects.html` is the full project catalogue and can grow as new work is completed.

Projects are ordered by technical depth, completeness, and relevance to AI/ML roles. Stronger and more recent work appears first.

## Current projects

| Rank | Project | Summary | Source | Live demo |
| ---: | --- | --- | --- | --- |
| 1 | AI Patent Intelligence Dashboard | Interactive analysis of 80,566 US AI patent records with filters, KPIs, trends, rankings, and downloadable data. | [GitHub](https://github.com/JanakDobariya/ai-patent-intelligence-dashboard) | [Open app](https://ai-patent-intelligence-dashboard.streamlit.app/) |
| 2 | YouTube AI Assistant | Transcript-grounded summarisation and question answering using semantic retrieval and Groq. | [GitHub](https://github.com/JanakDobariya/YouTube-Assistant) | [Open app](https://youtube-assistant-summarizer.streamlit.app/) |
| 3 | Movie Recommendation System | Content-based recommendations across 4,800 TMDB movies using TF-IDF vectors and cosine similarity. | Publishing soon | Publishing soon |
| 4 | Twitter Sentiment Classifier | Classifies short social-media text as negative, neutral, or positive with a trained scikit-learn model. | [GitHub](https://github.com/JanakDobariya/twitter-sentiment-classifier) | [Open app](https://twitter-sentiment-classifier.streamlit.app/) |
| 5 | Narad Muni Chatbot | Session-aware Streamlit chatbot powered by Groq's chat-completions API. | [GitHub](https://github.com/JanakDobariya/Narad-Muni-chatbot) | [Open app](https://narad-muni-chatbot.streamlit.app/) |
| 6 | Titanic Survival Predictor | Educational Streamlit interface for a trained gradient-boosting classification model. | [GitHub](https://github.com/JanakDobariya/titanic-streamlit-app) | [Open app](https://titanic-survival-dataset.streamlit.app/) |
| 7 | CampusCloud | Django academic portal with profiles, notes, notifications, quizzes, results, and campus tools. | [GitHub](https://github.com/JanakDobariya/CampusCloud-Project) | Not currently published |

## Run locally

### Option 1: open the files directly

Clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/JanakDobariya/portfolio.git
cd portfolio
open index.html
```

On Windows, replace the final command with:

```powershell
start index.html
```

### Option 2: use a local web server

Serving the folder is recommended because it behaves more like the deployed website:

```bash
git clone https://github.com/JanakDobariya/portfolio.git
cd portfolio
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser. Stop the server with `Ctrl+C`.

If `python3` is unavailable on Windows, try:

```powershell
py -m http.server 8000
```

## Offline use

The portfolio pages themselves work offline because all layout, styling, and JavaScript are inside the HTML files. No installation or compilation is required.

When fully offline:

- The browser uses fallback fonts because the preferred Google Fonts cannot be downloaded.
- GitHub, LinkedIn, email, and live-demo links require an internet connection.
- The deployed Streamlit applications are separate projects and do not run from this portfolio repository.

To run an individual Streamlit project locally, open its GitHub repository and follow that project's README. Most use the following workflow:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
streamlit run app.py
```

Some applications require an API key. Keep keys in environment variables or Streamlit secrets and never commit them to Git.

## Repository structure

```text
portfolio/
├── index.html       # Main portfolio and six featured projects
├── projects.html    # Complete ranked project catalogue
└── README.md        # Project documentation
```

## Updating the portfolio

When adding a project:

1. Add it to `projects.html` in the correct quality-ranked position.
2. Renumber the projects that follow it.
3. If it belongs in the strongest six, add it to `index.html` and remove the weakest featured project.
4. Include a concise description and only the technologies actually used.
5. Add separate Live Demo and GitHub links when they are available.
6. Update the project table in this README.

## Deployment

The production website is hosted on Vercel and connected to the `main` branch of this repository. Because the site is static, Vercel can publish it without a custom build command.

After pushing an update, allow Vercel a short time to build and publish the new deployment.
