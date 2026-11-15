# Wayleaf privacy policy

Last updated: **15 November 2026**

Wayleaf is a notes app that keeps your notes in a Git repository. This policy explains what the app
stores, what leaves your device, and where it goes.

The short version: **Wayleaf has no server, and the developer receives none of your data.** There is
no account to create, no analytics, and no telemetry. The only place your notes go is the Git remote
you choose yourself.

## What the developer collects

**Nothing.** There is no Wayleaf server, no developer-operated endpoint of any kind, and no
third-party analytics, crash-reporting or advertising code in the app. The developer has no way to
see your notes, your credentials, your usage, or whether you have ever opened the app.

## What is stored on your device

| What | Where | Notes |
|---|---|---|
| Your notes | A Git repository in the app's own storage area | Plain files, readable by the app only |
| Git credentials for your remotes | Encrypted storage (`EncryptedSharedPreferences`) | Encrypted with a key held in the Android keystore |
| App preferences | Ordinary app storage | Theme, sidebar layout, last note opened, draft commit message, auto-sync setting, the list of repositories you have added, and when each was last fetched |

All of this is held in storage private to Wayleaf. Uninstalling the app removes it.

### About your credentials

If you give Wayleaf a username and password or token to reach a Git remote, it is stored encrypted on
your device and used only to talk to that remote. It is never sent anywhere else.

Android may invalidate the encryption key in some circumstances — reinstalling the app, or changing
your device's screen lock, can both do it. If that happens, **Wayleaf discards the stored credentials
and you will be asked for them again.** This is deliberate: the app would rather lose a saved
password than fail to protect it.

## What leaves your device

Only what you push, and only to where you send it.

When you sync, Wayleaf connects to the Git remote you configured and transfers your notes to it. That
remote is yours — a service like GitHub or Azure DevOps, or your own server. **Its operator can see
what you send, and its own privacy policy governs what they do with it.** The developer of Wayleaf is
not involved in that transfer and cannot see it.

Git commits record an author name and email address. Wayleaf uses the ones you have configured, and
they travel with your commits to your remote, as they would with any Git client.

Wayleaf requests network access and network-state access for this syncing, and notification
permission so it can tell you when a background sync needs your attention. It asks for **no storage
permission at all** — your notes live in the app's own storage area, which needs none.

## Children

Wayleaf is a notes app with no social features, no user-generated content shared between users, and
no advertising. It collects nothing, so it collects nothing from children.

## Changes to this policy

This policy is kept in the app's source repository and changes to it are part of its version
history. The date at the top says when it last changed. If a future version of Wayleaf ever collects
anything, this policy will say so before that version ships.

## Contact

Questions about privacy in Wayleaf can be raised as an issue at
<https://github.com/wayleaf-app/wayleaf-privacy/issues>.
