# SplitPro Login Options and Configuration

### To start Docker, at least user authentication is required. The simplest option for this is likely the integration of a mail server.

## 1. Login via Email (Magic Link or Password)

### Description:
Users register with their email address. A Magic Link is sent, or they set a password.

### Required Variables:
| Variable               | Description                                           | Example Value                   |
|------------------------|-------------------------------------------------------|---------------------------------|
|  EMAIL_SERVER_HOST     | SMTP server host                                      |  smtp.gmail.com                 |
|  EMAIL_SERVER_PORT     | SMTP port                                             |  587  (TLS) or  465  (SSL)      |
|  EMAIL_SERVER_USER     | Email account username                                |  youremail@example.com          |
|  EMAIL_SERVER_PASSWORD | Email account password                                |  your-email-password            |
|  FROM_EMAIL            | Sender address displayed in the email header          |  noreply@example.com            |

---

## 2. Google OAuth

### Description:
Users log in with their Google account.

### Required Variables:
| Variable              | Description                                           | Example Value                   |
|-----------------------|-------------------------------------------------------|---------------------------------|
|  GOOGLE_CLIENT_ID     | Google OAuth Client ID                                |  your-google-client-id          |
|  GOOGLE_CLIENT_SECRET | Google OAuth Client Secret                            |  your-google-client-secret      |

### Steps:
1. Create a project in the [Google Cloud Console](https://console.cloud.google.com/).
2. Enable the "OAuth Consent Screen".
3. Create credentials for a web application.
4. Copy the Client ID and Client Secret into the variables.

---

## 3. GitHub OAuth

### Description:
Users log in with their GitHub account.

### Required Variables:
| Variable              | Description                                           | Example Value                   |
|-----------------------|-------------------------------------------------------|---------------------------------|
|  GITHUB_CLIENT_ID     | GitHub OAuth Client ID                                |  your-github-client-id          |
|  GITHUB_CLIENT_SECRET | GitHub OAuth Client Secret                            |  your-github-client-secret      |

### Steps:
1. Go to [GitHub Developer Settings](https://github.com/settings/developers).
2. Create a new OAuth app.
3. Set the **Homepage URL** to your app’s URL.
4. Set the **Authorization Callback URL** to  https://<your-app-domain>/api/auth/callback/github .
5. Copy the Client ID and Client Secret into the variables.

---

## 4. Facebook OAuth

### Description:
Users log in with their Facebook account.

### Required Variables:
| Variable                | Description                                           | Example Value                   |
|-------------------------|-------------------------------------------------------|---------------------------------|
|  FACEBOOK_CLIENT_ID     | Facebook OAuth Client ID                              |  your-facebook-client-id        |
|  FACEBOOK_CLIENT_SECRET | Facebook OAuth Client Secret                          |  your-facebook-client-secret    |

### Steps:
1. Go to [Meta for Developers](https://developers.facebook.com/).
2. Create a new app.
3. Enable "Facebook Login".
4. Set the OAuth Redirect URL to  https://<your-app-domain>/api/auth/callback/facebook .
5. Copy the Client ID and Client Secret into the variables.

---

## 5. Azure AD OAuth

### Description:
Users log in with their Azure Active Directory account.

### Required Variables:
| Variable                | Description                                           | Example Value                   |
|-------------------------|-------------------------------------------------------|---------------------------------|
|  AZURE_AD_CLIENT_ID     | Azure AD OAuth Client ID                              |  your-azure-ad-client-id        |
|  AZURE_AD_CLIENT_SECRET | Azure AD OAuth Client Secret                          |  your-azure-ad-client-secret    |
|  AZURE_AD_TENANT_ID     | Azure AD Tenant ID                                    |  your-azure-ad-tenant-id        |

### Steps:
1. Go to the [Azure Portal](https://portal.azure.com/).
2. Register a new app.
3. Set the **Redirect URL** to  https://<your-app-domain>/api/auth/callback/azure-ad .
4. Copy the Tenant ID, Client ID, and Client Secret into the variables.

---

## 6. Twitter OAuth

### Description:
Users log in with their Twitter account.

### Required Variables:
| Variable               | Description                                           | Example Value                   |
|------------------------|-------------------------------------------------------|---------------------------------|
|  TWITTER_CLIENT_ID     | Twitter OAuth Client ID                               |  your-twitter-client-id         |
|  TWITTER_CLIENT_SECRET | Twitter OAuth Client Secret                           |  your-twitter-client-secret     |

### Steps:
1. Go to the [Twitter Developer Portal](https://developer.twitter.com/).
2. Create a new app.
3. Set the Callback URL to  https://<your-app-domain>/api/auth/callback/twitter .
4. Copy the Client ID and Client Secret into the variables.

---

## 7. Custom OAuth Provider

### Description:
Integration of a custom OAuth provider.

### Required Variables:
| Variable                | Description                                           | Example Value                    |
|-------------------------|-------------------------------------------------------|----------------------------------|
|  CUSTOM_PROVIDER_ID     | Provider ID                                           |  your-provider-id                |
|  CUSTOM_PROVIDER_SECRET | Provider Secret                                       |  your-provider-secret            |
|  CUSTOM_PROVIDER_URL    | URL of the OAuth provider                             |  https://your-provider.com/oauth |

---
