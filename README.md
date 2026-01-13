# YOOM - Video Calling Application

YOOM is a modern video calling application built with Next.js, featuring real-time video conferencing, collaborative code editing, chat functionality, and screen sharing capabilities. It serves as a comprehensive Zoom-like platform for remote meetings and collaborative coding sessions.

## Demo

Check out our application in action:

[![Watch the demo](https://img.youtube.com/vi/6NKHB6UhRHM/maxresdefault.jpg)](https://www.youtube.com/watch?v=6NKHB6UhRHM)

## Features

- 🎥 Real-time video conferencing with multiple layout options
- 👥 Multi-user support with participant management
- 💬 Integrated chat system for communication
- 💻 Collaborative code editor with syntax highlighting
- 🌐 Support for multiple programming languages (JavaScript, TypeScript, Python, Java, C++, HTML, CSS)
- 🔐 Secure authentication with Clerk
- 📅 Calendar integration for scheduling meetings
- 🛡️ Anti-cheating measures (disabled keyboard shortcuts during meetings)
- 📹 Screen sharing and camera controls
- 📊 Meeting statistics and quality monitoring

## Tech Stack

- **Framework**: Next.js 14
- **UI Components**: Radix UI Primitives, Tailwind CSS
- **Video Conferencing**: Stream.io Video SDK
- **Authentication**: Clerk
- **Real-time Communication**: Socket.io
- **Code Execution**: EMKC Piston API
- **Code Editor**: Monaco Editor
- **Icons**: Lucide React
- **Styling**: Tailwind CSS with animations

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Dev2139/YOOM.git
cd YOOM
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env.local` file in the root directory with the following variables:
```env
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_STREAM_API_KEY=
STREAM_API_SECRET=
```

4. Run the development servers:
```bash
# Terminal 1: Start the Next.js app
npm run dev

# Terminal 2: Start the Socket.io server
node server.js
```

## Project Structure

```
├── actions/
│   └── stream.actions.ts          # Stream-related server actions
├── app/
│   ├── (auth)/                    # Authentication routes
│   ├── (root)/                    # Main application routes
│   │   ├── (home)/               # Home page and related components
│   │   └── meeting/[id]/         # Meeting room page
│   ├── globals.css               # Global styles
├── components/
│   ├── ui/                       # Reusable UI components
│   ├── MeetingRoom.tsx           # Core meeting room component
│   ├── MeetingSetup.tsx          # Pre-meeting setup component
│   ├── MeetingModal.tsx          # Modal dialogs
│   └── ...                       # Other components
├── constants/
│   └── index.ts                  # Application constants
├── hooks/                        # Custom React hooks
├── providers/
│   └── StreamClientProvider.tsx  # Stream client provider
└── server.js                     # Socket.io server for real-time features
```

## Key Components

### Meeting Room
The main meeting room component provides:
- Video conferencing with multiple layout options (grid, speaker-left, speaker-right)
- Participant list with mute/unmute controls
- Collaborative code editor with live synchronization
- Real-time chat functionality
- Anti-cheating measures to prevent tab switching during exams
- Screen sharing and recording capabilities

### Authentication
The application uses Clerk for secure authentication, providing:
- Sign-in/sign-up flows
- User session management
- Profile management
- Social login options

### Code Editor
Integrated Monaco Editor with:
- Syntax highlighting for multiple languages
- Real-time collaboration
- Code execution capabilities
- Output display panel
- Language selection

## Anti-Cheating Measures

To maintain academic integrity during online assessments, the application includes several anti-cheating measures:
- Disabling common keyboard shortcuts (Ctrl+Tab, Alt+Tab, F11, etc.)
- Preventing copy/paste operations during meetings
- Blocking right-click context menus
- Monitoring window focus events
- Notifications when participants switch tabs

## API Integration

The application integrates with external services:
- **Stream.io**: For video conferencing capabilities
- **EMKC Piston API**: For code execution in multiple programming languages
- **Clerk**: For authentication and user management

## Development

To contribute to this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add amazing feature'`)
5. Push to the branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

## Environment Variables

The application requires the following environment variables:

- `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY`: Clerk publishable key
- `CLERK_SECRET_KEY`: Clerk secret key
- `NEXT_PUBLIC_STREAM_API_KEY`: Stream.io API key
- `STREAM_API_SECRET`: Stream.io API secret

## Running Tests

To run the application in development mode:

```bash
npm run dev
```

The application will be available at `http://localhost:3000`.

## Deployment

The application is ready for deployment on platforms that support Next.js applications, such as Vercel, Netlify, or AWS.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with Next.js and the Stream.io Video SDK
- Special thanks to the open-source community for various libraries and tools used in this project
- Inspired by the need for secure, collaborative online learning environments
