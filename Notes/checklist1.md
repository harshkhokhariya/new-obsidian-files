This is the consolidated, final, and hyper-actionable list of to-dos. It blends the immediate launch tasks with the foundational development steps needed for the manual MVP.

Your focus is on **executing the launch plan** while simultaneously **creating the simplified local data environment** to support it.

---

### **Signal Scout: Immediate Action Plan (The Next 7 Days)**

This list is prioritized. **Start with the Launch Prep.**

#### **Phase A: Launch Prep & Marketing (The Shipper)**

| #      | Task                            | Description                                                                                                                                                | Status |
| :----- | :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------- | :----- |
| **A1** | **Build the Landing Page**      | Deploy a single-page site on **Cloudflare Pages**. Use the finalized copy: Headline, One-Liner Pitch, and the 3 Core Value Props.                          | - [  ] |
| **A2** | **Set Up Email Capture**        | Embed a simple **Google Form or ConvertKit** on the landing page to collect `Email`, `Product Description`, and `Target Subreddits`.                       | `[ ]`  |
| **A3** | **Create "Hottest Leads" List** | Generate a spreadsheet with the usernames and context of the 10 most relevant founders (from our reports) to target with personalized outreach.            | `[ ]`  |
| **A4** | **Targeted Outreach**           | Execute the "Giver" strategy (subtly linking the free report) to the 10 high-intent leads from the recent `r/indiehackers` keyword tracking post.          | `[ ]`  |
| **A5** | **Community Giver Content**     | Post 3 genuinely helpful comments (no promotion) in target communities, then add a P.S. to your profile directing traffic to the free report landing page. | `[ ]`  |

#### **Phase B: Local Development Environment (The Builder)**

| # | Task | Description | Status |
| :--- | :--- | :--- | :--- |
| **B1** | **Create Project Structure** | Create the root folders: `/backend/`, `/frontend/`, `/local_storage/`. | `[ ]` |
| **B2** | **Initialize Python Project** | In `/backend/`, create a virtual environment, install core dependencies (`fastapi`, `uvicorn`, `sqlite3`, `praw`, `litellm`, `pandas`), and create a placeholder `main.py`. | `[ ]` |
| **B3** | **SQLite DB Setup** | In the backend code, implement the initial creation of the **`Posts`**, **`Comments`**, and **`Users`** tables in the `database.db` file. | `[ ]` |
| **B4** | **Frontend Placeholder** | In `/frontend/`, create a simple HTML/JS file and run `npm run dev` to confirm it's working. | `[ ]` |
| **B5** | **Build the Internal Analytics Dashboard**| Create a simple **Streamlit** application (or a Jupyter Notebook) that connects to `database.db` and can execute a simple query (e.g., `SELECT * FROM Users`). | `[ ]` |

#### **Phase C: Script Integration & Automation**

| # | Task | Description | Status |
| :--- | :--- | :--- | :--- |
| **C1** | **Integrate `clean_reddit_dumps.py` Logic** | Refactor the core cleaning logic from `clean_reddit_dumps.py` into a reusable Python function inside your `/backend` library. | `[ ]` |
| **C2** | **Update Scraper to DB Insertion** | Update the Reddit scraper logic to no longer write `.txt` files, but to clean the data *in memory* and insert the structured records directly into the **`Posts`** and **`Comments`** SQLite tables, ensuring the **`scraped_at`** timestamp is correct. | `[ ]` |
| **C3** | **Refine `promo_hunter.py` Logic** | Modify the core analysis script to: **1)** Query the SQLite DB for comments/posts within the last 24 hours, and **2)** Run the LLM analysis only on the resulting, filtered text. | `[ ]` |

---

Your most important immediate next step is **A1, A2, and A3**. Get the funnel built and start the outreach. Focus on getting those first beta users, as their needs will guide the rest of your development.