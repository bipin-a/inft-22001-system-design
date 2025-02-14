# **Assignment: Designing an ML Application as an API**

### **Objective**
The goal of this assignment is to develop documentation that outlines the design process for an ML application that will be deployed as an API. This documentation will serve as a blueprint for an upcoming project where students will implement, train, evaluate, and deploy an ML model as a cloud-based API using Docker.

I suggest looking into Miro https://miro.com/app/dashboard/ or app.diagrams https://app.diagrams.net/ or Lucid Chart https://www.lucidchart.com/ for your diagram needs.

### **Scope of the Assignment**
You are required to prepare the following documentation:

1. **Use Case Diagram**
   - Define the actors interacting with your ML API in production.
   - Identify the main use cases
        - What is your model predicting?
        - How will features be sent into the model at time of inference?
        - How will you monitor the model's performance?
   - Show relationships between actors and use cases (e.g., include/extend relationships).

2. **Activity Diagram(s)**
   - Provide a step-by-step workflow for how data flows through the ML API at time of inference into the model, and then how the prediction is sent back to the user.
        - Think of data types, possible examples of values etc. 
   - Cover the process from data collection to deployment and API prediction (what feature values will be passed).
   - Include decision points (e.g., performance evaluation metrics).
   - **Hint:** You need to make two activity diagrams, one for RnD (model creation) and another for Production (model inference). Think about the steps from collecting data, preprocessing, training, evaluating and how they fall in RnD. And think of deploying the model as an API and gathering features at time of inference and the model making a prediction as Production.

3. **Development Methodology for Prototyping**
   - Choose a methodology (e.g., Throwaway Prototyping, Agile, Waterfall, Iterative).
   - Justify why this methodology is suitable for developing your ML API.
   - Outline how you would execute development steps following the chosen methodology.
   - **Hint:** Consider an iterative approach since ML models require continuous refinement.

4. **Video Explaination (Worth 50% for each section above)**
   - Share your screen and webcam and walk me through diagrams and methodology.
   - Explain your thought process and how you can to the answer.
   - Video should be less than 10 mins, otherwise you will lose marks.
   - If you read from a script, you will lose marks.
   - You may record your screen while in a Teams meeting that includes only yourself.

---

### **Project Preparation Details**
This assignment is meant to prepare you for a hands-on project where you will:
- **Build a Machine Learning Model**: Train a model using an open-source dataset on a straightforward classification or regression task.
- **Evaluate Model Performance**: Decide whether the model is fit for deployment.
- **Deploy the Model as an API**: Use Docker to containerize your application and deploy it on a cloud platform.

**Key Constraints:**
- No backend development required at this stage.
- No frontend development needed.

---

### **Submission Guidelines**
- **Use Case Diagram**: Highlight actor-system interactions.
- **Activity Diagram**: Show workflow with clear decision points.
- **Methodology**: 1-paragraph rationale for your chosen approach.

**Dataset Suggestion:** Choose a simple, well-structured dataset such as the Iris species classification dataset.

**Evaluation Criteria:**
- **Clarity and correctness** of diagrams (40%)
- **Logical structure and completeness** of the methodology explanation (30%)
- **Justification of the chosen methodology** in the context of ML API development (30%)

**Video Submission Note**:
- 50% of each component will be weighted by your video explanation.
- You must submit a video that includes a face cam recording of your screen. Look into software like OBS, or you may record your screen while in a Teams meeting that includes only yourself.
- If you read from a script, you will **not** get full marks.
- Guide me through your submission: Diagrams and Methodology.
- If the video is over 10 minutes long, you will lose marks. Keep it within 10 minutes.
