# Privacy Policy

**Last Updated:** December 2025

## Overview

OneDrive Photos & Videos Dupes is committed to protecting your privacy. This policy explains how we collect, use, and protect your data.

## Data Collection

### What We Collect

OneDrive Photos & Videos Dupes collects minimal data to provide and improve our service:

- **OneDrive File Metadata**: Names, sizes, dates, and checksums for duplicate detection
- **App Usage Analytics** (optional): Feature usage, scan statistics, error rates
- **Crash Reports** (optional): Stack traces, device info, app state when crashes occur

### What We DO NOT Collect

- File contents (photos, videos, documents)
- Personal information beyond OneDrive account authentication
- Location data
- Contacts or device identifiers

## Analytics & Crash Reports

### Firebase Integration

When enabled, OneDrive Photos & Videos Dupes uses:

- **Firebase Analytics**: Track app usage patterns and feature adoption
- **Firebase Crashlytics**: Identify and fix app crashes

### User Control

- **Default**: Analytics enabled (helps improve the app)
- **Opt-out**: Settings → Privacy → Analytics & Crash Reports toggle
- **Debug builds**: Always enabled for development
- **Release builds**: Respects user preference

### Data Collected

**Analytics Events:**
- `app_started` - App launch tracking
- `login_success` / `login_failure` - Authentication events
- `scan_started` / `scan_completed` - Duplicate detection operations
- `files_deleted` - File deletion operations
- `settings_changed` - User preference changes

**Crash Data:**
- Stack traces and error messages
- Device model and OS version
- App version and build number
- Memory and CPU state at crash time

## Data Storage

### Local Storage

- **File cache**: Stored in app's private directory on device
- **User preferences**: Stored using Android DataStore
- **Cleared**: Automatically when app is uninstalled

### Remote Storage

- **Analytics data**: Firebase (Google Cloud Platform)
- **Crash reports**: Firebase Crashlytics
- **No file contents**: Never transmitted or stored remotely

## Third-Party Services

### Microsoft OneDrive

- **Purpose**: File access and management
- **Data**: Authentication tokens, file metadata
- **Privacy Policy**: https://privacy.microsoft.com

### Firebase (Google)

- **Purpose**: Analytics and crash reporting (optional)
- **Data**: Usage events, crash logs
- **Privacy Policy**: https://firebase.google.com/support/privacy

## Data Retention

| Data Type | Retention Period | Location |
|-----------|------------------|----------|
| Local cache | Until app uninstalled | Device only |
| Analytics | 14 months (configurable) | Firebase |
| Crash reports | 90 days | Firebase Crashlytics |
| Authentication tokens | Until logout/expiry | Device only |

## Your Rights

You have the right to:

1. **Opt-out**: Disable analytics and crash reporting anytime
2. **Delete**: Remove all local data by uninstalling the app
3. **Access**: Request information about collected data
4. **Transparency**: Understand how your data is used

## Security

### Data Protection

- All file analysis performed **locally on device**
- Authentication via **Microsoft OAuth 2.0**
- Secure HTTPS connections for all API calls
- No plaintext storage of sensitive data

### Open Source

- Source code available at: https://github.com/nrgsh8kr/OneDriveMediaOps
- Transparent implementation, open to security review

## Privacy by Design

### Minimal Collection

- Only collect data necessary for app functionality
- No tracking of individual users
- No selling of user data

### User Control

- Clear opt-in/opt-out mechanisms
- Transparent privacy settings
- Easy access to this policy in-app

## Compliance

### Android Permissions

OneDrive Photos & Videos Dupes requests minimal permissions:

- **Internet**: Required for OneDrive API access
- **No storage permissions**: Uses OneDrive API, not device storage
- **No location**: Never tracks location
- **No contacts**: Never accesses contacts

### GDPR & Privacy Regulations

- Data minimization principle
- User consent for optional features
- Right to access and deletion
- Transparent data practices

## Changes to This Policy

We may update this privacy policy periodically. Changes will be:

1. Posted in the app (Settings → Privacy → View Privacy Policy)
2. Documented in this file with updated date
3. Communicated in release notes for major changes

## Contact

### Questions or Concerns

- **Email**: info@nrgsh8kr.com

### Data Requests

To request data deletion or access, email info@nrgsh8kr.com with:

1. Subject: "Privacy Request"
2. Your OneDrive account identifier
3. Type of request (deletion, access, etc.)

## Developer Notes

### For Contributors

If adding new data collection:

1. Update this privacy policy
2. Add user controls/opt-out mechanisms
3. Minimize data collection scope
4. Document in code comments

### Testing Privacy Settings

```bash
# Enable analytics debug mode
adb shell setprop debug.firebase.analytics.app com.onedrive.mediaops

# View analytics events
adb logcat -s FA FA-SVC

# Clear app data (reset privacy preferences)
adb shell pm clear com.onedrive.mediaops
```

## Summary

**Key Points:**

✅ **Minimal data collection** - Only what's necessary  
✅ **User control** - Opt-out anytime  
✅ **Local processing** - Files never leave device  
✅ **Transparent** - Open source code  
✅ **Secure** - OAuth 2.0 authentication  
✅ **No selling data** - Never, ever  

---

**Your privacy matters.** If you have concerns or suggestions, please open an issue on GitHub.
