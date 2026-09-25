# Privacy Policy

**Last Updated:** September 2026

## Overview

OneDrive Photos & Videos Dupes is committed to protecting your privacy. This policy explains how we collect, use, and protect your data.

## Data Collection

### What We Collect

- **OneDrive file metadata** (names, sizes, dates, thumbnails): read through Microsoft's API and processed **on your device** for duplicate detection. It is not sent to our servers.
- **App usage analytics** (optional, on by default): sign-in, scan and delete steps, counts, durations and error types, sent to Google Firebase Analytics.
- **Crash and error reports** (optional, on by default): stack traces, error messages and app state, sent to Google Firebase Crashlytics.
- **Collected automatically with analytics and crash reports**: device model, OS and app version, language, Firebase app-instance and installation IDs, and approximate location (country/region) that Google derives from your IP address.

### What We DO NOT Collect

- File contents (photos, videos, documents)
- Your Microsoft password (sign-in is handled by Microsoft)
- Precise location, contacts or advertising IDs

## Analytics & Crash Reports

### Firebase Integration

When enabled, OneDrive Photos & Videos Dupes uses:

- **Firebase Analytics**: Track app usage patterns and feature adoption
- **Firebase Crashlytics**: Identify and fix app crashes

### User Control

- **Default**: Analytics enabled (helps improve the app)
- **Opt-out**: the Analytics & Crash Reports switch in the Privacy section of the scan settings screen (shown after you choose folders to scan). Data sent before you turn it off is not recalled.
- **Debug builds**: Always enabled for development
- **Release builds**: Respects user preference

### Data Collected

**Analytics events** (parameters are counts, durations, outcome codes and error types; never file names or contents):
- App start and sign-in: `app_started`, `login_attempt`, `login_success`, `login_failure`, `login_cancelled`, `login_abandoned`, `silent_auth_completed`, `msal_init_failed`
- Scans: `scan_started`, `scan_completed`, `scan_cancelled`, `scan_failed`, `scan_interrupted`, `fgs_start_blocked`
- Deletion: `files_deleted`, `delete_failed`
- Settings: `settings_changed`
- Plus Firebase's automatic events (e.g. first open, session start, screen view, engagement time)

**Crash data:**
- Stack traces and error messages
- Device model, OS version, app version and build number
- Memory and storage usage at crash time
- Diagnostic keys (e.g. scan phase, folder count, demo mode, last sign-in outcome)
- Firebase installation ID

## Data Storage

### Local Storage

- **File cache**: Stored in app's private directory on device
- **User preferences**: Stored using Android DataStore
- **Cleared**: Automatically when app is uninstalled

### Remote Storage

- **Analytics data**: Firebase (Google Cloud Platform)
- **Crash reports**: Firebase Crashlytics
- **Analysis copies**: analytics and crash data are exported to our Google Cloud (BigQuery) project
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
| Analytics | Firebase's configured retention period | Firebase |
| Crash reports | 90 days | Firebase Crashlytics |
| Analytics and crash exports | Until we delete them | Our BigQuery project |
| Authentication tokens | Until sign-out/expiry | Device only |

## Your Rights

You have the right to:

1. **Opt-out**: Disable analytics and crash reporting anytime (Analytics & Crash Reports switch, scan settings screen)
2. **Delete**: Remove all local data by uninstalling the app, and ask us (info@nrgsh8kr.com) to delete analytics and crash data linked to your install
3. **Access**: Request information about collected data
4. **Transparency**: Understand how your data is used

## Security

### Data Protection

- All file analysis performed **locally on device**
- Authentication via **Microsoft OAuth 2.0**
- Secure HTTPS connections for all API calls
- No plaintext storage of sensitive data

## Privacy by Design

### Minimal Collection

- Only collect data necessary for app functionality
- No advertising, ad IDs or cross-app tracking
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

1. Posted in the app (scan settings screen → Privacy → View Privacy Policy)
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
✅ **Transparent** - Every analytics event is listed above  
✅ **Secure** - OAuth 2.0 authentication  
✅ **No selling data** - Never, ever  

---

**Your privacy matters.** If you have concerns or suggestions, please email info@nrgsh8kr.com.
