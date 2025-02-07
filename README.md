# 🤖 AI Chatbot Project
Welcome to the AI Chatbot project! This chatbot leverages Google's Gemini API to provide intelligent responses. Follow the steps below to set up and customize your chatbot.

## 🖥️ Preview
![Preview](https://github.com/user-attachments/assets/3cd0f632-23a9-4ccd-b26f-d64556403083)

If you encounter an error like "API key not valid. Please pass a valid API key." while using the Chatbot, follow these steps:

## 🔑 Getting a Free API Key
### If you encounter an error like "API key not valid. Please pass a valid API key.", follow these steps:
1. Go to Google AI Studio[Google AI Studio](https://aistudio.google.com/app/apikey).
2. Navigate to the API Key section and create a new API key (it's free!).
3. Your API key will look something like this: AIzaSyAtpnKGX13bTgmx0l_gQeatYvdWvY_wOTQ

## 🔧Setting Up Your API Key

1. Open your project folder in VS Code.
2. Navigate to the `script.js` file.
3. Find the `API_KEY` variable and replace `PASTE-YOUR-API-KEY` with your actual API key.

## Save and Test

1. Save the `script.js` file after adding your API key.
2. Open `index.html` in your browser to verify that Chatbot is working correctly.

## 🎨 Customization

This chatbot can be customized to better suit your needs. You can personalize it by adding your company details.

### ✏️ Modify Chat History

Update lines 24 and 40 in the script.js file:

```javascript
// Line 24
const chatHistory = [
  {
    role: "model",
    parts: [{ text: `Your company information here` }],
  },
];

// Line 40
chatHistory.push({
  role: "user",
  parts: [{ text: `Using the details provided above, please address this query: ${userData.message}` }, ...(userData.file.data ? [{ inline_data: userData.file }] : [])],
});
```

## 🔄 Switching to a Stable Model

The chatbot currently uses Gemini-1.5-Flash (beta), allowing more free requests within a shorter timeframe. However, for greater reliability, you can switch to Gemini-1.5-Pro.

### 🔁 Update API URL in script.js

const API_URL = `https://generativelanguage.googleapis.com/v1/models/gemini-1.5-pro:generateContent?key=${API_KEY}`;

#### ⚠️ Note: The free version of gemini-1.5-pro has stricter request limits. Consider upgrading to a paid plan for unlimited access.

### ⭐ Show Your Support

If you like this project, give it a ⭐ on GitHub! Your support motivates means a lot for me. 😊

## 👤Contributor

- [Vadym Makohon](https://github.com/VadymMakohon)
