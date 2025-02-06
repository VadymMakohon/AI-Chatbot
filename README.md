# AI Chatbot Project
Welcome to the AI Chatbot project! This chatbot leverages Google's Gemini API to provide intelligent responses. Follow the steps below to set up and customize your chatbot.

## 🖥️ Preview
![Preview](https://github.com/user-attachments/assets/3cd0f632-23a9-4ccd-b26f-d64556403083)

If you encounter an error like "API key not valid. Please pass a valid API key." while using the Chatbot, follow these steps:

## 🔑 Getting a Free API Key
### If you encounter an error like "API key not valid. Please pass a valid API key.", follow these steps:
1. Go to Google AI Studio[Google AI Studio](https://aistudio.google.com/app/apikey).
2. Navigate to the API Key section and create a new API key (it's free!).
3. Your API key will look something like this: AIzaSyAtpnKGX13bTgmx0l_gQeatYvdWvY_wOTQ

## Insert Your API Key

1. Open your project folder in VS Code.
2. Navigate to the `script.js` file.
3. Find the `API_KEY` variable and replace `PASTE-YOUR-API-KEY` with your actual API key.

## Save and Test

1. Save the `script.js` file after adding your API key.
2. Open `index.html` in your browser to verify that Chatbot is working correctly.

## Customization Tips

This chatbot uses the free Gemini API to generate responses to any questions. You can customize it by adding your company information, and the chatbot will respond accordingly.

Simply update lines 24 and 40 of `script.js` file with the following code:

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

## Important Information

This chatbot uses the Gemini beta model, gemini-1.5-flash, which allows more free requests within a shorter timeframe. If you need greater reliability, you can switch to the stable model, gemini-1.5-pro. While the free version of this model has stricter request limits, upgrading to a paid plan will remove these restrictions.

To switch to the gemini-1.5-pro stable model, update the API_URL in the `script.js` file as follows:
const API_URL = `https://generativelanguage.googleapis.com/v1/models/gemini-1.5-pro:generateContent?key=${API_KEY}`;

### ⭐ Show Your Support

If you like this project, give it a ⭐ on GitHub! Your support motivates means a lot for me. 😊

## 👤Contributor

- [Vadym Makohon](https://github.com/VadymMakohon)
