
# 🎬 Content Generator App

An AI-powered web application that generates **videos, social media posts, and other content** based on your prompts using OpenAI's GPT model.

## ✨ Features

- **📹 Video Script Generation** - Create detailed video scripts for TikTok, Instagram Reels, and YouTube Shorts
- **📱 Social Media Posts** - Generate engaging posts for Instagram, TikTok, Twitter, Facebook, and LinkedIn
- **✨ General Content** - Create blog posts, newsletters, ads, and more
- **🎯 Customizable Options** - Choose tone, style, duration, and platform
- **💾 Copy to Clipboard** - Easy copying of generated content

## 🛠️ Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- OpenAI API Key (sign up at https://platform.openai.com)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/fatimahali2831-svg/content-generator-app.git
   cd content-generator-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create `.env` file**
   ```bash
   cp .env.example .env
   ```
   
   Then edit `.env` and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   PORT=5000
   ```

4. **Start the server**
   ```bash
   npm start
   ```
   
   Or for development with auto-reload:
   ```bash
   npm run dev
   ```

5. **Open in browser**
   - Go to `http://localhost:5000`
   - Start creating content!

## 📚 How to Use

### Video Script Tab
1. Enter what your video is about
2. Choose duration (15s, 30s, or 60s)
3. Select a style (entertaining, educational, funny, etc.)
4. Click "Generate Script"
5. Copy the generated script

### Social Post Tab
1. Enter what you want to post about
2. Choose the platform (Instagram, TikTok, Twitter, etc.)
3. Select tone (casual, professional, funny, etc.)
4. Click "Generate Post"
5. Copy and use on your social media

### General Content Tab
1. Describe what you want to create
2. Choose content type (blog post, email, ad, etc.)
3. Select tone
4. Click "Generate Content"
5. Copy the result

## 📁 Project Structure

```
content-generator-app/
├── server.js              # Main server file
├── package.json           # Dependencies
├── .env.example           # Environment variables template
├── .gitignore             # Git ignore file
├── README.md              # This file
└── public/
    ├── index.html         # Main webpage
    ├── styles.css         # Styling
    └── script.js          # Frontend JavaScript
```

## 🔌 API Endpoints

### POST `/api/generate-video-script`
Generates a detailed video script.

**Request:**
```json
{
  "topic": "How to make coffee",
  "duration": "30",
  "style": "entertaining"
}
```

**Response:**
```json
{
  "success": true,
  "script": "...",
  "topic": "How to make coffee",
  "duration": "30"
}
```

### POST `/api/generate-post`
Generates a social media post.

**Request:**
```json
{
  "topic": "My new product launch",
  "platform": "Instagram",
  "tone": "casual"
}
```

**Response:**
```json
{
  "success": true,
  "post": "...",
  "topic": "My new product launch",
  "platform": "Instagram"
}
```

### POST `/api/generate`
Generates any type of content.

**Request:**
```json
{
  "prompt": "Create a funny meme about coding",
  "contentType": "video",
  "tone": "funny"
}
```

**Response:**
```json
{
  "success": true,
  "content": "...",
  "contentType": "video",
  "prompt": "Create a funny meme about coding"
}
```

## 💡 Tips

- Be specific in your prompts for better results
- Use different tones to test which works best for your audience
- The app provides content ideas, but you may need to edit for your specific needs
- Keep your OpenAI API key secret - never share it publicly

## 🚀 Deployment

### Deploy to Heroku
1. Install Heroku CLI
2. Run `heroku login`
3. Run `heroku create your-app-name`
4. Set environment variables: `heroku config:set OPENAI_API_KEY=your_key`
5. Run `git push heroku main`

### Deploy to Vercel (with serverless functions)
- Requires converting to serverless architecture
- Use Vercel's API routes instead of Express

## 📊 Cost Considerations

- This app uses OpenAI's API, which has usage costs
- Estimated cost: $0.002 - $0.01 per generation (varies by content length)
- Monitor your usage at https://platform.openai.com/account/usage

## 🐛 Troubleshooting

### "Invalid API key"
- Check that your OpenAI API key is correct in `.env`
- Make sure your OpenAI account has credits

### "Port 5000 is already in use"
- Change PORT in `.env` to another number (e.g., 5001)
- Or kill the process using port 5000

### "CORS error"
- The app includes CORS headers, but check browser console for details
- Ensure your frontend and backend are communicating correctly

## 📝 License

MIT License - Feel free to use this project for personal or commercial use.

## 🤝 Contributing

Have ideas for improvements? Feel free to:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

If you have questions:
- Check the README and API documentation first
- Review the code comments
- Check OpenAI's documentation at https://platform.openai.com/docs

---

**Made with ❤️ by Copilot**

Happy creating! 🎉
