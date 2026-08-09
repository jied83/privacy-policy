# Privacy Policy — Baby Logger

**Effective date:** 9 August 2026
**Last updated:** 9 August 2026
**Application:** Baby Logger (Android package `de.jied.babylogger`)

## 1. Who is responsible

The data controller within the meaning of Art. 4(7) GDPR is:
> Email: **forgottenfork2025@gmail.com**

If you have any question about this policy or about your data, write to the address above. We answer
data-protection requests within 30 days.

## 2. The short version

Baby Logger is a diary app for parents. Everything you record is stored **on your own device**. There is
**no Baby Logger server and no Baby Logger account** — we operate no backend, and we cannot read, copy or
recover the diary entries you create.

If — and only if — you switch on synchronisation, the app writes a copy of your data into **your own
Google Drive**, using your own Google account. Even then the data stays between you and Google; it never
passes through us.

The only information that reaches us is anonymous, aggregated crash and usage statistics from Google
Firebase, described in section 6.

## 3. What data the app processes

### 3.1 Data you enter yourself (stored on your device)

| Data | Examples | Where it is stored |
|---|---|---|
| Child profile | Name or nickname of the child, date of birth | Local database on your device |
| Diary definitions | Diary names, icons, field templates you create | Local database on your device |
| Diary entries | Timestamp plus the values of each field, and an optional free-text note | Local database on your device |
| App settings | Theme, per-diary chart preference | Local database on your device |

**Health data about a child.** The built-in diaries — and any diary you build yourself — are intended for
information such as **body temperature, medication name and dose, feeding, sleep and nappy changes**. Under
Art. 9(1) GDPR this is health data about a minor, i.e. a special category of personal data. It is processed
**exclusively on your device** and, if you enable sync, in **your own Google Drive**. We never receive it.

The app does not ask for, and cannot access, your contacts, photos, precise location, microphone, camera or
call data. The Android app declares **no runtime permissions** at all.

### 3.2 Data processed when you enable Google Drive synchronisation (optional)

Synchronisation is off by default. You start it yourself in *Settings → Account & sync*. When you sign in
with Google:

- The app requests exactly one OAuth scope: **`https://www.googleapis.com/auth/drive.file`**. This scope is
  deliberately the narrowest one Google offers for this purpose — it grants access **only to files this app
  itself created, or that you explicitly picked**. The app cannot see, list or read the rest of your Drive.
- The app creates and maintains **a single file in your Drive**, named `babylogger-sync.json` (content type
  `application/vnd.babylogger.sync+json`). It contains a snapshot of your children, diaries and entries so
  that another device signed in to the same account can restore them.
- The **email address of the signed-in Google account** is stored locally, only so the app can show you
  which account is connected.
- Access tokens issued by Google are held in memory / by Google Play services for the duration of the
  session and are not transmitted anywhere except to Google's own APIs.

That file lives in **your** Drive, under **your** control, and counts against **your** storage quota. We
have no access to it.

### 3.3 Data processed when you share a family library (optional)

You may give a second person — typically the other parent — access to the same data:

- You type **their Google account email address**. The app sends it to Google's Drive API in order to grant
  that account write access to your `babylogger-sync.json` file. Google then emails them a notification.
- The app can display the list of people who currently have access to that file (email address and role),
  read back from Google Drive.
- Accepting an invitation on the other device uses the **Google Picker**, in which that person selects the
  shared file. Their device then replaces its local data with the shared library.

Sharing means **transferring the child's data, including the health data described in 3.1, to another
person's Google account**. You choose who that is, and you can revoke access at any time — in the app or
directly in Google Drive.

### 3.4 Data collected automatically (Google Firebase)

See section 6.

### 3.5 Advertising

**The app currently displays no advertising and contains no advertising SDK.** A future version is planned
to show ads via **Google AdMob**; section 7 describes that in advance. This policy will be updated, with a
new "last updated" date, **before** any ad SDK actually ships, and the Google Play data-safety declaration
will be updated at the same time.

## 4. Why we process it, and on what legal basis

| Purpose | Data | Legal basis |
|---|---|---|
| Providing the app's core function — keeping your diaries | Section 3.1 | Art. 6(1)(b) GDPR (performance of a contract), and for health data your explicit consent, Art. 9(2)(a) GDPR — given by entering it |
| Synchronising and backing up your data across your devices | Sections 3.1, 3.2 | Your consent, Art. 6(1)(a) and Art. 9(2)(a) GDPR — given by signing in and enabling sync; withdrawable at any time |
| Sharing a library with a second person | Section 3.3 | Your consent, Art. 6(1)(a) and Art. 9(2)(a) GDPR — given by sending the invitation |
| Diagnosing crashes and keeping the app stable | Section 6, Crashlytics | Art. 6(1)(f) GDPR — our legitimate interest in a functioning app |
| Understanding aggregate feature usage | Section 6, Analytics | Art. 6(1)(f) GDPR — our legitimate interest in improving the app |
| Advertising (future) | Section 7 | Your consent, Art. 6(1)(a) GDPR |

You may withdraw any consent at any time with effect for the future — see section 9.

## 5. Who receives your data

We do **not** sell personal data, and we do not pass it to advertising networks or data brokers.

Data reaches third parties only in these cases:

- **Google Ireland Ltd. / Google LLC** — as the operator of Google Drive, Google Sign-In and Firebase. When
  you enable sync, your data is stored in your own Google Drive under [Google's Privacy
  Policy](https://policies.google.com/privacy) and your own agreement with Google.
- **The person you invite** to a shared library (section 3.3), if you send such an invitation.
- **Google Play** — only aggregated, anonymous statistics that Google itself derives from installs; we
  never receive individual identities through it.

**International transfers.** Google may process data outside the European Economic Area, including in the
United States. Google relies on the European Commission's standard contractual clauses and on the EU–US
Data Privacy Framework for these transfers.

## 6. Firebase Analytics and Firebase Crashlytics

The Android app includes Google Firebase (Crashlytics and Analytics). These are **active in the current
version**. They are the only components that send anything to us — and only in a form that does not
identify you.

**Firebase Crashlytics** collects, when the app crashes or misbehaves:

- stack traces and exception details,
- device model, operating-system version, app version,
- device state at the moment of the crash (free memory, storage, orientation, whether the device was
  rooted),
- a randomly generated installation identifier (Crashlytics Installation UUID).

**Firebase Analytics** collects:

- app instance ID (a random, resettable identifier),
- events such as app start, screen views and app updates,
- device model, operating-system version, app version, language and country,
- coarse geographic region derived from the IP address (the IP address itself is not stored long-term by
  Google Analytics for Firebase).

**Neither service receives any diary content** — no child names, no dates of birth, no temperatures,
medications, notes or any other entry data. We do not set a user ID and we do not send custom parameters
containing your data.

Data retention at Google: Crashlytics reports are kept for up to **90 days**; Analytics event data for up
to **14 months**. Details: [Firebase Privacy and Security](https://firebase.google.com/support/privacy).

## 7. Advertising via Google AdMob (planned, not yet active)

When advertising is introduced, this section will apply:

- Ads will be delivered by **Google AdMob** (Google Ireland Ltd.).
- AdMob may use the **Android advertising ID (AAID)** and technical data — device type, operating-system
  version, coarse location derived from the IP address, ad interactions — to select and measure ads, and to
  limit how often the same ad is shown.
- **No diary data of any kind will be passed to AdMob.** The advertising SDK has no access to the local
  database or to your Drive file.
- Users in the EEA, the UK and Switzerland will be shown a **consent dialog** (Google's User Messaging
  Platform / IAB TCF) before any personalised advertising, and may decline. Declining means
  non-personalised ads, not loss of app functionality.
- The Android advertising ID can be reset or deleted at any time under *Settings → Google → Ads* on your
  device.
- Google's own information: [How Google uses information from sites or apps that use our
  services](https://policies.google.com/technologies/partner-sites).

Adding the ad SDK will require the `com.google.android.gms.permission.AD_ID` permission; the app declares
no permissions today.

## 8. How long we keep data

- **Diary data on your device** — until you delete it in the app, clear the app's data, or uninstall the
  app. There is no automatic expiry; the whole point of a diary is that it is kept.
- **The sync file in your Drive** — until you delete it yourself. Uninstalling the app does not remove it.
- **Crashlytics / Analytics** — the Google retention periods stated in section 6.

## 9. Deleting your data and withdrawing consent

Because there is no server, deletion is entirely in your hands. To remove everything:

1. **Local data** — delete individual entries, diaries or children in the app; or remove all of it at once
   via *Android Settings → Apps → Baby Logger → Storage → Clear data*, or by uninstalling the app.
2. **The synchronised copy** — open [drive.google.com](https://drive.google.com), delete the file
   **`babylogger-sync.json`**, and empty the Drive bin. This also ends access for anyone you shared it
   with.
3. **The app's access to your Google account** — go to
   [myaccount.google.com/permissions](https://myaccount.google.com/permissions) and remove Baby Logger.
   Note that revoking this access also drops the per-file sharing grants the app had set up, so a person
   you invited may lose access as a result.
4. **Sharing only** — to stop sharing without deleting anything, remove that person in the app, or remove
   their access to the file in Google Drive.

Withdrawing consent (signing out, revoking access) does not affect the lawfulness of processing carried out
before the withdrawal.

## 10. Your rights

Under the GDPR you have the right to:

- **access** the personal data we process about you (Art. 15),
- **rectification** of inaccurate data (Art. 16),
- **erasure** (Art. 17),
- **restriction** of processing (Art. 18),
- **data portability** (Art. 20) — the app has a built-in export to CSV and JSON, which gives you your
  complete data in a machine-readable form at any time, without asking us,
- **object** to processing based on legitimate interests (Art. 21),
- **withdraw consent** at any time (Art. 7(3)),
- **lodge a complaint with a supervisory authority** (Art. 77). In Germany this is the data-protection
  authority of the federal state in which the controller is based; you may also complain to the authority
  where you live or work.

For data you hold yourself, most of these rights are exercised directly in the app — nothing needs to go
through us. For the Firebase data described in section 6, write to **forgottenfork2025@gmail.com**.

## 11. Children

Baby Logger is intended for **parents and carers, i.e. adults**. It is not directed at children and is not
designed for use by children.

The app does, however, hold data **about** children, entered by their parent or legal guardian. That person
is the one who decides what is recorded and who it is shared with. Where consent is required for the
processing of a child's data, it is given by the holder of parental responsibility.

We do not knowingly collect data directly from children. If you believe a child has entered data into the
app in circumstances that require our attention, contact us at the address in section 1.

## 12. Security

- Diary data is stored in the app's private storage area, which on Android is not readable by other apps.
- All communication with Google's APIs uses **HTTPS/TLS**.
- The app requests the narrowest available Google Drive scope (`drive.file`, see section 3.2) rather than
  full Drive access.
- We hold no copy of your data, so there is no central database of ours that could be breached.

Please note that the security of the synchronised copy also depends on the security of your Google account
— use a strong password and two-factor authentication.

## 13. Changes to this policy

We may update this policy, for instance when new features (such as advertising) are added. The current
version is always available at the URL published on the app's Google Play listing. Material changes will be
announced in the app before they take effect. The "last updated" date at the top of this document shows the
current revision.

## 14. Contact

> Email: **forgottenfork2025@gmail.com**
