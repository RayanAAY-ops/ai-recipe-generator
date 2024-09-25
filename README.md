### Key Steps
![Capture d’écran 2024-09-25 à 16 56 21](https://github.com/user-attachments/assets/135206f2-c554-4ebc-803b-2a4beba66ea9)
1. **AWS Amplify Hosting**:
   - **Initialize and configure Amplify** to host your frontend.
     - This step ensures your **HTML-based UI** for submitting ingredients is hosted with **continuous deployment** enabled via GitHub.
   - **Link**: Frontend deployment ensures users can access the app for ingredient submission.

2. **Amplify Auth Setup**:
   - Add **Amplify Auth** to enable user login and authentication using **Amazon Cognito**.
   - **Link**: Auth secures access to the app, ensuring only authenticated users can submit ingredient requests to the backend.

3. **Amazon Bedrock & Claude 3 Sonnet Access**:
   - Set up permissions for the backend to access **Amazon Bedrock** and integrate the **Claude 3 Sonnet model** to generate recipes.
   - **Link**: Bedrock provides AI model access, allowing the backend to generate recipes based on user-inputted ingredients.

4. **Backend Application Using AWS Lambda**:
   - Create a **serverless backend** with AWS Lambda and API Gateway using Amplify API.
   - **Link**: The Lambda function processes ingredient submissions from the frontend and interacts with the Claude 3 Sonnet model via Bedrock.

5. **Amplify DataStore Integration**:
   - Configure **Amplify DataStore** to connect the frontend to the backend.
   - **Link**: DataStore facilitates the seamless flow of data between the frontend (ingredient submission) and backend (recipe generation).

6. **Frontend-Backend Connection**:
   - Implement **API calls** in the frontend to send user-submitted ingredients to the backend for processing.
   - **Link**: This connection ensures that when a user submits ingredients, the backend requests an AI-generated recipe from Bedrock and returns it to the frontend.

### Overall Flow:
1. **User inputs ingredients** ➡️ 
2. **Frontend sends data** to backend (via Amplify API) ➡️ 
3. **Lambda function processes request** (uses Bedrock for AI generation) ➡️ 
4. **Recipe is returned to frontend** for display to the user.

