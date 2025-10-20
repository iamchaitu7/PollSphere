# PollSphere Code Migration Guide

## Overview
This guide will help you manually migrate code from Rocket.new to this GitHub repository due to Rocket.new plan limitations.

## Current Status
✅ GitHub repository created: `iamchaitu7/PollSphere`
✅ README with comprehensive documentation added
✅ Flutter .gitignore configured

## Required: Manual Code Migration

Due to Rocket.new's plan restrictions (token limit exhausted and download feature requires upgrade), you'll need to manually copy the code files.

### Option 1: Upgrade Rocket.new Plan (Recommended)
1. Visit your Rocket.new project: https://www.rocket.new/688780338cb4050014930750
2. Click "Upgrade" button
3. Choose a plan that includes code export
4. Download the complete project as a ZIP file
5. Extract and push to this GitHub repository

### Option 2: Manual File-by-File Copy

#### Project Structure (69 files total)
```
PollSphere/
├── .dart_tool/
├── android/
├── assets/
├── ios/
├── lib/
│   ├── core/
│   ├── presentation/
│   ├── routes/
│   ├── theme/
│   ├── utils/
│   ├── widgets/
│   └── main.dart
├── supabase/
│   └── migrations/
│       └── 20250128141625_pollsphere_complete_schema.sql
├── web/
├── .flutter-plugins
├── .flutter-plugins-dependencies
├── .gitignore (✅ Already added)
├── env.json
├── pubspec.lock
├── pubspec.yaml
└── README.md (✅ Already added)
```

#### Steps to Copy Files:

1. **Open Rocket.new Project**
   - Go to: https://www.rocket.new/688780338cb4050014930750?type=2&f=NLC_FLUTTER#code
   - Navigate to the Code tab

2. **For Each File:**
   - Click on the file in the file tree (left panel)
   - Select all content in the editor (Ctrl+A / Cmd+A)
   - Copy the content (Ctrl+C / Cmd+C)
   - Come to GitHub and create the file with same path
   - Paste the content
   - Commit the file

3. **Priority Files to Copy (Start with these):**
   
   **Essential Configuration:**
   - `pubspec.yaml` - Flutter dependencies
   - `env.json` - Environment configuration
   - `pubspec.lock` - Dependency lock file
   
   **Core Application:**
   - `lib/main.dart` - App entry point
   - All files in `lib/core/` - Core services
   - All files in `lib/presentation/` - UI screens
   
   **Database:**
   - `supabase/migrations/*.sql` - Database schema
   
   **Key Service Files (mentioned in Rocket.new):**
   - `supabase_service.dart`
   - `auth_service.dart`
   - `poll_service.dart`
   - `admin_service.dart`

4. **Platform-Specific Files:**
   - Copy `android/` folder files for Android support
   - Copy `ios/` folder files for iOS support
   - Copy `web/` folder files for web support
   - Copy `assets/` folder for images/resources

### Option 3: Using GitHub Web Interface

1. **Upload Multiple Files:**
   - Go to repository main page
   - Click "Add file" → "Upload files"
   - Drag and drop files (if you can access them locally)

2. **Create Folders:**
   - To create a folder, use "/" in filename
   - Example: `lib/core/constants.dart` will create lib/core/ folder

### Option 4: Using Git CLI (If you have files locally)

```bash
# Clone the repository
git clone https://github.com/iamchaitu7/PollSphere.git
cd PollSphere

# Copy your code files here
# Then push
git add .
git commit -m "Add PollSphere source code from Rocket.new"
git push origin main
```

## Important Files to Include

### Configuration Files
- ✅ `.gitignore` - Already configured with Flutter template
- ⏳ `pubspec.yaml` - Flutter project configuration
- ⏳ `env.json` - Supabase and OAuth credentials
- ⏳ `.flutter-plugins` - Flutter plugin registry
- ⏳ `.flutter-plugins-dependencies` - Plugin dependencies

### Environment Variables (`env.json`)
Make sure to include but **DO NOT commit sensitive values**:
```json
{
  "SUPABASE_URL": "your-supabase-url",
  "SUPABASE_ANON_KEY": "your-anon-key",
  "GOOGLE_CLIENT_ID": "your-google-client-id",
  "APPLE_CLIENT_ID": "your-apple-client-id"
}
```

## Key Features Implemented (from Rocket.new)

According to your Rocket.new project, the following features are implemented:

### Screens (11 total):
1. ✅ Splash Screen
2. ✅ Authentication Screen (Google/iOS OAuth)
3. ✅ Onboarding Flow
4. ✅ Poll Feed
5. ✅ Poll Detail
6. ✅ Poll Creation
7. ✅ Search Screen
8. ✅ User Profile
9. ✅ Notifications
10. ✅ Settings
11. ✅ Admin Dashboard

### Integrations:
- ✅ Supabase integration with authentication services
- ✅ Database schema for polls, users, votes, comments
- ✅ Google/Apple OAuth authentication
- ✅ Real-time voting and updates
- ✅ Admin dashboard functionality

### Test Credentials (from Rocket.new):
**Regular Users:**
- Email: john.doe@gmail.com | Password: password123
- Email: sarah.wilson@icloud.com | Password: password123
- Username: alex_pollster | Password: password123

**Admin:**
- Email: admin@pollsphere.com | Password: AdminPass123

## Next Steps

1. Choose one of the migration options above
2. Copy all 69 files from Rocket.new to GitHub
3. Verify the project structure matches
4. Update `env.json` with your credentials (don't commit sensitive data)
5. Test the application locally:
   ```bash
   flutter pub get
   flutter run
   ```

## Support

If you encounter issues:
1. Check file paths match the structure above
2. Ensure all dependencies in `pubspec.yaml` are correct
3. Verify Supabase configuration in `env.json`
4. Run `flutter doctor` to check Flutter setup

## Contact

For questions about this migration or the PollSphere app, please open an issue in this repository.

---

**Repository:** https://github.com/iamchaitu7/PollSphere
**Rocket.new Project:** https://www.rocket.new/688780338cb4050014930750
**Created:** October 21, 2025
