# GitHub Enterprise – Developer Onboarding

Welcome! Follow these steps to get access set up. Read through the whole guide before you start — the order matters.

---

## Step 1 – Create or confirm your GitHub account

You need a GitHub account to access your org. If you don't have one, create one at [github.com](https://github.com) using your **corporate email address**.

You must create a new GitHub account using your **corporate email address**. Personal GitHub accounts are not permitted for accessing org resources.

---

## Step 2 – Enable Two-Factor Authentication (2FA)

Your org requires 2FA on all GitHub accounts. If your account doesn't have it enabled, you will be blocked from accessing the org.

1. Go to **GitHub → Settings → Password and authentication → Two-factor authentication**
2. Enable 2FA using one of the approved methods: **authenticator app, passkey, or security key**

> ⚠️ SMS-based 2FA is not accepted. You must use an authenticator app (e.g. Microsoft Authenticator) or a hardware security key.

---

## Step 3 – Accept Your Invitation Email(s)

You will receive two invitation emails from GitHub:

1. **Enterprise invitation** – grants you access to your org's enterprise account
2. **Organization invitation** – grants you access to the `your-org` org and its repositories

**Accept any invitations you receive.** If you received two, accept them in order — enterprise first, then org.

> 📧 **Check your junk/spam folder** — these emails frequently get filtered. Outlook users should also check the **Non-Productive Mail** folder.

---

## Step 4 – Authorize SSO

This step links your GitHub account to your corporate identity. It is required even if you were able to accept the invitations without it.

1. Go to **[https://myapps.microsoft.com](https://myapps.microsoft.com)**
2. Select the **SSO tile provided by your admin** and sign in with your corporate credentials
3. Then go to the **SSO authorization link provided by your admin** and click **Authorize**

> ⚠️ If you skip this step, your GitHub account will not be recognized as an org member and you may lose access to org resources in the future.

---

## Step 5 – Verify Access

Confirm you can see the `your-org` organization and the repositories your team should have access to.

If you can see the org but not any repositories, you may not have been added to a team yet — this is an admin action. Contact your admin or [your contact / IT / Slack channel].

If anything else is missing or you encounter an error, reach out before trying again.

---

## Step 6 – Enable Your No-Reply Email

GitHub can mask your real email address in commit metadata and notifications. Enabling this protects your corporate email from being exposed publicly.

1. Click your **profile picture** (top-right corner) → **Settings**
2. In the left sidebar, select **Emails**
3. Check **"Keep my email addresses private"**
4. GitHub will generate a no-reply address in the format `ID+username@users.noreply.github.com` — this is the address that will appear on your commits

> ℹ️ If you use Git locally, update your local Git config to use this no-reply address so your commits stay private:
> ```
> git config --global user.email "ID+username@users.noreply.github.com"
> ```
> Copy the exact address shown on the GitHub Emails settings page.

---

## Troubleshooting

| Issue | Fix |
|---|---|
| Didn't receive an invitation email | Check spam/junk and the **Non-Productive Mail** folder in Outlook. Contact your admin if still missing. |
| SSO redirect fails | Clear browser cache and cookies, then try again |
| Can't see org repos after accepting invitations | Make sure you completed Step 4 (SSO authorization). If that's done, contact your admin — you may not have been added to a team yet. |
| Prompted to create a new account | Stop — sign in to your existing GitHub account instead, then complete Step 4 |
| Blocked due to 2FA | Your GitHub account needs 2FA enabled with an approved method. See Step 2. |
| SSO authorization says you don't have access | Confirm with your admin that you have been added to the appropriate SSO-enabled GitHub group in Entra. |
