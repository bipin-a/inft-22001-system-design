# **Final Project: Enhanced Data Analysis and Visualization App**

## **Objective**

For your final project, you’ll enhance the application you started in **Assignment 2 (A2)**—the initial phase of your data analysis app. Use the feedback provided in class and your **Assignment 3 (A3)** self-reflection (where you analyzed your process through the lens of software lifecycle, Agile, and planning) to improve your work. This project adds a **Streamlit frontend**, three new features, and an optional deployment for bonus marks. Improvement doesn’t mean piling on complexity—sometimes simplifying your code or UI makes a bigger impact!

> **NOTE**: It’s okay if your app isn’t flawless. Like we discussed in class, focus on learning and explaining your choices. If something doesn’t work perfectly, tell me why, what you tried, and the pros and cons in your demo video. You’re graded on effort, reflection, and growth, not perfection!

---

## **Functional Requirements**

Your project builds on your A2 FastAPI backend (e.g., a spam detector, sales predictor, or other data-driven app). You’ll add a Streamlit frontend and three new features, reflecting on how your A3 insights (e.g., Agile iterations, planning gaps) shaped your approach.

### 1. **Streamlit Frontend**
- Create a user-friendly interface using **Streamlit** to interact with your FastAPI backend’s endpoints (e.g., `/predict`, `/data`).
- Host Streamlit on a different port (e.g., 8501) from FastAPI (e.g., 8000). Use Python’s `requests` library in Streamlit to call FastAPI endpoints.
- Design a clean, intuitive UI based on **Week 10 lecture notes**:
  - Include input fields (e.g., text box for email input if doing spam detection).
  - Show results clearly (e.g., “Spam” or “Not Spam” with confidence scores).
  - Add buttons or sliders for user interaction (e.g., “Submit” or “Adjust threshold”).
- Keep it simple—no need for fancy CSS. Focus on:
  - Clear labels (e.g., “Enter your email here”).
  - Logical layout (use `st.columns` or tabs).
  - Feedback (e.g., “Processing…” or error messages if input fails).

> **Why Streamlit?** It’s like a quick dashboard builder for Python. You write simple code, and it turns into a web app users can click around in.

---

### 2. **Feature 1: Beeswarm Plot for SHAP- Replace your A2 Matplotlib plots (if any) with a **Plotly Beeswarm plot** to visualize **SHAP values** for your model’s predictions.
- SHAP (from Week 8) explains why your model made a prediction (e.g., “This email is spam because it has ‘free’ and a weird link”).
- Use `plotly.express` or `plotly.graph_objects` to create an interactive Beeswarm plot (see [Plotly Beeswarm Docs](https://plotly.com/python/beeswarm/)).
- Example: If your app predicts spam, show a dot for each feature (like “word_count” or “has_link”) and its SHAP value (how much it pushed toward “spam” or “not spam”).
- Display the plot in Streamlit using `st.plotly_chart`.
- Make it interactive: Users can hover to see feature details or zoom in.

> **What’s a Beeswarm?** Imagine a swarm of bees—each bee is a dot showing a feature’s impact. It’s clearer than Matplotlib’s static bars and lets users explore!

---

### 3. **Feature 2: Data Validation with Great Expectations**
- Add **Great Expectations** to check your input data before it hits your model.
- Example (for spam detection):
  - Ensure input is a string and contains “@” for email addresses.
  - Check text length (e.g., not empty, not over 5000 characters).
- Example (for numeric data, like sales prediction):
  - Ensure numbers aren’t negative if they shouldn’t be (e.g., “sales” ≥ 0).
  - Set a min/max range (e.g., “price” between 0 and 10000).
- Use at least **two expectations** (rules) for your data.
- Show validation results in Streamlit (e.g., “Input valid!” or “Error: Missing ‘@’”).
- Check the [Great Expectations Quickstart](https://docs.greatexpectations.io/docs/guides/setup/) for setup (takes ~10 minutes).

> **Why validate?** Bad input (like “123” for an email) can crash your model. Great Expectations is like a gatekeeper checking data before letting it through.

---

### 4. **Feature 3: Data Contract**
- Export your FastAPI’s **OpenAPI schema** to define your API’s data contract (covered in Week 7).
- Two ways to do this:
  1. Run in terminal: `curl http://localhost:<your_port>/openapi.json > openapi_schema.json`.
  2. Or visit `http://localhost:<your_port>/openapi.json` in your browser and save the file.
- Include the `openapi_schema.json` file in your submission.
- In your demo video, explain:
  - What the schema shows (e.g., endpoints like `/predict`, expected inputs/outputs).
  - Why it’s useful (e.g., “It’s a contract so others know how to use my API”).

> **What’s a data contract?** It’s like a menu for your API—shows what it can do and what it needs. Takes 1 minute to export!

---

### 5. **FastAPI Backend**
- Keep your A2 FastAPI backend (e.g., endpoints for predictions, data retrieval).
- Update based on A2 feedback (e.g., fix bugs, simplify routes).
- Add new endpoints if needed:
  - For SHAP values (e.g., `/explain` to return feature impacts).
  - For Great Expectations results (e.g., `/validate` to check input).
- Ensure Streamlit can call all endpoints smoothly (test with `requests.get` or `requests.post`).

---

### 6. **Reflection and Agile Connection**
- Use your **A3 reflection** (from Agile, software lifecycle, planning) to guide improvements:
  - **Planning**: Did A3 show you underplanned A2? Set clearer tasks this time (e.g., “Day 1: Set up Streamlit”).
  - **Agile**: Treat this project as a new sprint. Break work into small chunks (e.g., “Get Beeswarm plot working by Wednesday”).
  - **Lifecycle**: Think about maintenance—did A2’s code make adding features hard? Refactor if needed (e.g., split big functions).
- In your demo video, explain how A3’s lessons shaped your work (e.g., “In A3, I realized my tests were weak, so I added Great Expectations”).

> **Why reflect?** It’s like a post-game analysis—helps you avoid past mistakes and build better.

---

### 7. **Deployment (Optional for Bonus Marks)**
- For **5% bonus marks**, deploy your app to **Google Cloud Run** using **Docker Compose**.
- Write a `docker-compose.yml` to run:
  - **Streamlit container** (port 8501).
  - **FastAPI container** (port 8000).
- Create a `Dockerfile` for each:
  - Use `python:3.9-slim` as the base image.
  - Install dependencies (e.g., `streamlit`, `fastapi`, `great-expectations`, `shap`, `plotly`).
- Steps:
  1. Build: `docker-compose build`.
  2. Push to Google Container Registry: `gcloud builds submit`.
  3. Deploy: `gcloud run deploy`.
- Share the Cloud Run URL in your submission.
- **Docker Compose Resources**:
  - [Official Docker Compose Docs](https://docs.docker.com/compose/) – Basics of `docker-compose.yml`.
  - [Docker Compose for Python](https://docs.docker.com/compose/gettingstarted/) – Python example.
  - [Google Cloud Run Guide](https://cloud.google.com/run/docs/quickstarts/build-and-deploy) – Deployment steps.

> **Why deploy?** It’s like putting your app online for the world to see. Bonus marks for trying!

---

### 8. **Visualization**
- Show results in Streamlit:
  - Input and output (e.g., “Email: free@deal.com → Spam (90%)”).
  - Beeswarm plot for SHAP (interactive dots showing feature impacts).
  - Validation status (e.g., “Input OK” or “Error: Invalid email”).
- Keep it clear:
  - Use colors (e.g., green for valid, red for errors).
  - Avoid clutter—space out elements with `st.markdown` or columns.
- (Optional) Add a small table or graph for extra stats (e.g., prediction history).

---

## **Demonstration Video Requirements**

Record a **5–7 minute** video showcasing your app. Focus on:
- **App walkthrough**:
  - Upload data or input in Streamlit.
  - Show predictions, Beeswarm plot, and validation results.
  - (If deployed) Open the Cloud Run URL to prove it’s live.
- **Algorithms and features**:
  - Explain SHAP and Beeswarm (e.g., “SHAP shows why my model said ‘spam’—these dots highlight key words”).
  - Describe Great Expectations (e.g., “It checks if emails have ‘@’ to avoid crashes”).
  - Pros and cons (e.g., “Beeswarm is interactive but slow for big datasets”).
  - If results aren’t perfect, say why (e.g., “My model missed some spam because…”).
- **System overview**:
  - How Streamlit calls FastAPI (e.g., “I send the email to `/predict` and get back a score”).
  - Role of the data contract (e.g., “The schema lists all my endpoints”).
- **Reflection**:
  - How A3’s lessons helped (e.g., “In A3, I saw I rushed testing, so I planned better”).
  - What you learned (e.g., “SHAP made my model less of a black box!”).
  - Limits (e.g., “Validation missed edge cases like…”).
- Be **precise**—no rambling. Plan your points but don’t read a script. Talk like you’re explaining to a classmate who knows Python but not SHAP or APIs.
- **Tip**: Rehearse once to cut filler words (e.g., “um”). Keep it clear and engaging.

---

## **Testing Instructions**
Test your app with:
1. **Your A2 dataset** (e.g., spam emails, sales records).
2. **Edge cases**:
   - Invalid inputs (e.g., “no_at_symbol” for email, negative sales).
   - Tricky data (e.g., ambiguous emails like “free trial”).
Test to:
- Ensure Great Expectations catches bad inputs.
- Confirm Beeswarm plots show clear SHAP values.
- Verify Streamlit-FastAPI communication (no 404 errors).
- (If deployed) Check Cloud Run responds fast.

---

## **Submission Requirements**
- Source code (Streamlit frontend, FastAPI backend).
- `openapi_schema.json` (data contract).
- (If bonus) `docker-compose.yml`, `Dockerfile`(s), and deployment instructions.
- Demonstration video (5–7 minutes).

---

## **Support**
- **Stuck?** DM me on Teams—I respond quickly!
- **Confused?** Ask about SHAP, Great Expectations, or Docker in Teams.
- I’m here to help you succeed!

---

You’ve built a solid foundation in A2 and reflected deeply in A3. Now’s your chance to polish and learn something new—keep it simple, have fun, and show me what you’ve got!

