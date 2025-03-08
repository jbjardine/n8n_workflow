# n8n Custom Auth Credential Updater

This workflow is specifically designed for quickly and securely updating your n8n Custom Auth credentials automatically on your self-hosted n8n instance.

## 🚀 How it works:

The workflow automates updating your n8n authentication token for credentials of type **httpCustomAuth**. It:

1. **Authenticates to your n8n instance** using your provided login credentials.
2. **Generates a UUID v4** to simulate a browser session for enhanced security.
3. **Retrieves the list of credentials** currently stored in your n8n instance.
4. **Filters and updates** only the credential matching the provided name (`name_credential`).
5. **Automatically formats and injects the new token** provided.

---

## 🚀 Quick Start

### Prerequisites:
In your workflow, configure the following in the **Login credentials** node:

- **n8n URL** *(example: `https://n8n.yourdomain.com`)*
- **n8n email** *(your n8n user email)*
- **n8n password** *(your n8n user password)*

### Workflow Input Parameters:

When calling this workflow, provide:

- **`name_credential`** *(string)*: Name of your existing Custom Auth credential in n8n.
- **`value_credential`**: The new token value to update your Custom Auth credential (**without** the `Bearer` prefix—just the raw token).

### Features

- **Automatic token formatting**: No need to handle prefixes manually.
- **Multi-update capability**: Update multiple credentials by calling this workflow repeatedly.
- **Error handling**: Provides clear error messages to simplify troubleshooting.

### Ideal Use Case
Perfect for automating credential rotations, enhancing security, or integrating with external systems requiring regular token updates.

## 🚀 How to import

1. Download the workflow JSON:  
   [⬇️ Download Workflow JSON](https://raw.githubusercontent.com/jbjardine/n8n_workflow/main/update_credential_custom_auth/template.json)

2. Import it into your n8n instance via:
   - **Workflow → Import → From file**

---

**Made with ❤️ by jbjardine**
