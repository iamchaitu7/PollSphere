# PollSphere

A comprehensive social polling platform built with Flutter and Supabase, featuring real-time poll updates, social media functionality, and admin dashboard capabilities.

## 🌟 Features

### User Features
- **Authentication**: Google and iOS authentication with Supabase
- **Poll Creation**: Create polls from various templates
- **Real-time Voting**: Live poll results and updates
- **Social Feed**: Browse and interact with public polls
- **Comments & Engagement**: Comment on polls and interact with other users
- **User Profiles**: Personalized user profiles with poll history
- **Search**: Find polls and users easily
- **Notifications**: Stay updated on poll activity
- **Settings**: Customize app preferences

### Admin Features
- **Admin Dashboard**: Comprehensive management interface
- **Content Moderation**: Review and moderate polls
- **Analytics**: Track platform usage and engagement
- **User Management**: Manage users and permissions

## 🏗️ Architecture

### Technology Stack
- **Frontend**: Flutter (Dart)
- **Backend**: Supabase
- **Authentication**: Supabase Auth with OAuth (Google, Apple)
- **Database**: PostgreSQL (via Supabase)
- **Real-time**: Supabase Realtime subscriptions

### Project Structure
```
lib/
├── core/           # Core functionality and services
├── presentation/   # UI screens and widgets
├── routes/         # Navigation and routing
├── theme/          # App theming and styling
├── utils/          # Utility functions and helpers
├── widgets/        # Reusable UI components
└── main.dart       # App entry point

supabase/
└── migrations/     # Database schema and migrations
```

### Key Screens
1. **Splash Screen**: App initialization
2. **Authentication Screen**: Login/signup with Google/iOS
3. **Onboarding Flow**: First-time user experience
4. **Poll Feed**: Main feed with all public polls
5. **Poll Detail**: Detailed poll view with voting and comments
6. **Poll Creation**: Create polls with templates
7. **Search Screen**: Search functionality
8. **User Profile**: View and edit user profiles
9. **Notifications**: Activity notifications
10. **Settings**: App configuration
11. **Admin Dashboard**: Admin management interface

## 🚀 Getting Started

### Prerequisites
- Flutter SDK (latest stable version)
- Dart SDK
- Supabase account and project
- Android Studio / Xcode for mobile development

### Installation

1. Clone the repository:
```bash
git clone https://github.com/iamchaitu7/PollSphere.git
cd PollSphere
```

2. Install dependencies:
```bash
flutter pub get
```

3. Configure Supabase:
   - Create a Supabase project
   - Update `env.json` with your Supabase credentials
   - Run the database migrations from `supabase/` folder

4. Run the app:
```bash
flutter run
```

## 🔑 Test Credentials

For testing purposes, use these credentials:

**Regular Users:**
- Email: john.doe@gmail.com | Password: password123
- Email: sarah.wilson@icloud.com | Password: password123
- Username: alex_pollster | Password: password123

**Admin:**
- Email: admin@pollsphere.com | Password: AdminPass123

## 📱 Supported Platforms
- ✅ iOS
- ✅ Android
- ✅ Web

## 🔧 Configuration

### Environment Variables
Update `env.json` with your configuration:
```json
{
  "SUPABASE_URL": "your-supabase-url",
  "SUPABASE_ANON_KEY": "your-anon-key",
  "GOOGLE_CLIENT_ID": "your-google-client-id",
  "APPLE_CLIENT_ID": "your-apple-client-id"
}
```

## 📊 Database Schema

The database schema includes:
- **users**: User profiles and authentication
- **polls**: Poll data and metadata
- **poll_options**: Options for each poll
- **votes**: User votes on polls
- **comments**: Comments on polls
- **notifications**: User notifications
- **admin_actions**: Admin activity logs

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [Flutter](https://flutter.dev/)
- Backend powered by [Supabase](https://supabase.com/)
- Generated using [Rocket.new](https://rocket.new/)

## 📞 Contact

For questions or support, please open an issue in this repository.
