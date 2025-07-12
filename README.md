# Login.only

A responsive login page built with vanilla HTML, CSS, and JavaScript, designed to be deployed on Vercel with Supabase authentication.

## 🚀 Features

- ✅ **Responsive design** that works on all devices
- ✅ **Clean, minimal UI** using only black, white, and light gray
- ✅ **Supabase authentication** integration
- ✅ **Form validation** (email format, password length)
- ✅ **Error handling** with user-friendly messages
- ✅ **Environment variable** configuration
- ✅ **Ready for Vercel deployment**

## 📁 Project Structure

```
Login_only/
├── .env.local              ← Private environment variables (not in repo)
├── scripts/
│   └── generate-env.js     ← Generates login/config.js from env vars
├── login/                  ← All website files
│   ├── index.html          ← Dashboard (root page)
│   ├── login.html          ← Login page
│   ├── login.css           ← Responsive styling
│   ├── login.js            ← Login functionality
│   ├── auth.js             ← Authentication manager
│   ├── dashboard.js        ← Dashboard functionality
│   └── config.js           ← Generated from environment variables
├── vercel.json             ← Vercel deployment configuration
└── README.md               ← This file
```

## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/stoiccapital/login.only.git
cd login.only
```

### 2. Environment Variables

Create a `.env.local` file in the root directory with your Supabase credentials:

```bash
# Supabase Configuration
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_ANON_KEY=your-anon-key-here
```

### 3. Generate Config File

Run the environment generation script:

```bash
node scripts/generate-env.js
```

This will create `login/config.js` with your environment variables.

### 4. Local Development

Serve the files locally:

```bash
cd login && python3 -m http.server 3000
```

Then visit `http://localhost:3000`

## 🚀 Deployment to Vercel

### 1. Install Vercel CLI

```bash
npm install -g vercel
```

### 2. Deploy

```bash
vercel
```

### 3. Set Environment Variables

In your Vercel dashboard:
1. Go to your project settings
2. Navigate to "Environment Variables"
3. Add:
   - `SUPABASE_URL` = your Supabase project URL
   - `SUPABASE_ANON_KEY` = your Supabase anon key

## 🎨 UI Components

- **Logo placeholder**: Circular "F" logo
- **Headline**: "Welcome back to Finmetic"
- **Email input**: Validates email format
- **Password input**: Minimum 6 characters
- **Login button**: Black background, white text
- **Forgot password link**: Placeholder for password reset

## 🔐 Authentication Features

- **Session management**: Users stay logged in across browser sessions
- **Protected routes**: Dashboard requires authentication
- **Guest protection**: Logged-in users can't access login page
- **Automatic redirects**: Based on authentication status
- **Proper logout**: Clears session and redirects

## 🎯 Color Scheme

The design uses only three colors:
- `#000` (black) - Primary text, buttons, logo
- `#fff` (white) - Background, button text
- `#f5f5f5` (light gray) - Page background, input borders

## 🔒 Security Considerations

- Environment variables are not exposed in client-side code
- Supabase anon key is safe for client-side use
- Form validation prevents unnecessary API calls
- Error messages don't expose sensitive information

## 🌐 Browser Support

- Modern browsers with ES6+ support
- Mobile browsers (iOS Safari, Chrome Mobile)
- Desktop browsers (Chrome, Firefox, Safari, Edge)

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📞 Support

If you have any questions or issues, please open an issue on GitHub. 