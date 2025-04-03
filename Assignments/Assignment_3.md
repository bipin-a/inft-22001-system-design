# Assignment 3: Systems Analysis & Design Reflection

## Overview
This assignment builds on Assignment 2, where you deployed a machine learning (ML) model using FastAPI on Google Cloud Run. You will reflect on your development process through the lens of systems analysis and design methodologies covered in this course, including the systems development life cycle (SDLC) and approaches like waterfall, iterative, and agile. The goal is to critically evaluate your approach, analyze technical challenges, and propose design improvements.

## Learning Objectives
- Evaluate the effectiveness of your systems development approach.
- Apply systems analysis concepts to reflect on your implementation.
- Propose how proper design methodologies could address technical challenges.

---

## Part 1: Systems Development Methodology Analysis (40%)

### 1.1 Development Approach Evaluation
- Identify the systems development methodology you followed in Assignment 2 (e.g., waterfall, iterative, agile). If you didn’t explicitly choose one, infer the closest match based on your process.
- Analyze how this methodology influenced your approach to:
  - **Requirements Gathering**: How did you determine what the system needed to do?
  - **Design Decisions**: How did you plan the model, API, and deployment?
  - **Implementation Strategy**: How did you execute the coding and deployment?
  - **Testing and Validation**: How did you verify the system worked as intended?
- Provide specific examples (e.g., “I iterated on the API design after testing, reflecting an agile approach”) and discuss how your methodology impacted your project’s success or challenges.

### 1.2 Systems Development Life Cycle (SDLC) Analysis
- Map your Assignment 2 process to the SDLC phases: planning, analysis, design, implementation, and maintenance.
- For each phase:
  - Did you complete it? If so, how thoroughly?
  - Which phases received adequate attention, and which were rushed or overlooked?
- Identify one technical challenge (e.g., deployment delays) and explain how it stemmed from shortcomings in a specific SDLC phase (e.g., insufficient planning).

**NOTE**: Each problem you encountered should be mapped to an SDLC phase.

---

## Part 2: Requirements & Design Analysis (40%)

### 2.1 Requirements Analysis
- Describe how you gathered and documented requirements for Assignment 2 (e.g., assumed needs, trial-and-error).
- Identify at least one **implicit requirement** you discovered during development (e.g., “The API needed to handle larger datasets than expected”).
- Explain how more thorough requirements analysis (e.g., stakeholder interviews, use cases, defining an MVP) could have prevented a specific challenge.
- Reflect on how your requirements evolved as you worked—did this align with your methodology?

### 2.2 Design Decisions & Tradeoffs
- Document key design decisions you made for:
  - **Model Selection**: Why did you choose your ML model?
  - **API Architecture**: How did you structure your FastAPI endpoints?
  - **Deployment Strategy**: Why Google Cloud Run, and how did you configure it?
- For each decision:
  - What alternatives did you consider (e.g., Flask instead of FastAPI)?
  - What factors influenced your choice (e.g., time, familiarity)?
  - How did this decision impact the final implementation (e.g., performance, complexity)?
  - Suggest one design pattern or principle (e.g., modularity, separation of concerns) that could have improved your solution.

---

## Part 3: Technical Challenge Analysis & Future Recommendations (20%)

### 3.1 Challenge Analysis
Select **three technical challenges** from Assignment 2 and analyze them through a systems analysis and design perspective. **Focus on depth over breadth—1–2 strong paragraphs per challenge are sufficient**. Examples include:
- Model selection and evaluation (e.g., difficulty assessing overfitting).
- Data preprocessing (e.g., inconsistent data formats).
- Environment setup and dependency management (e.g., Python version conflicts).
- API design and schema implementation (e.g., Pydantic errors).
- Deployment and cloud infrastructure (e.g., Google Cloud Run memory limits).
- Performance optimization (e.g., slow API responses).

For each challenge:
- Describe the problem in detail (e.g., “Dependencies failed to load on a different machine”).
- Link it to a systems analysis/design concept (e.g., inadequate requirements analysis, poor design modularity).
- Explain how applying a course methodology (e.g., iterative testing in agile) could have prevented or mitigated it.

### 3.2 Future Recommendations
Based on your analysis, briefly outline improvements for a similar project:
- Suggest one systems development methodology (e.g., agile) and why it fits.
- Identify one SDLC phase to emphasize (e.g., analysis) and explain why.
- Describe one change to your requirements or design approach (e.g., “I’d define an MVP first. Keep It Simple, Then Optimize.”).

---

## Submission Requirements
- **Format**: PDF
- **Length**: 2-4 pages, single-spaced.
- **Visual Elements**: Include 1–2 optional diagrams (if useful, e.g., SDLC mapping, API architecture). Visuals are not required but may clarify your analysis. Focus on quality of reflection over visuals.


## Evaluation Criteria
- **Application of Systems Analysis and Design Concepts (50%)**: Depth of connection to SDLC and methodologies.
- **Critical Analysis of Development Approach (30%)**: Insightfulness and specificity of reflection.
- **Quality of Proposed Design Improvements (20%)**: Feasibility and relevance of suggestions.
