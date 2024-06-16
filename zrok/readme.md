# Zrok

## Installation

1. **Download Zrok**: Get the latest Windows executable from the [Zrok GitHub releases page](https://github.com/openziti/zrok/releases).
2. **Extract Files**: Extract the downloaded zip file to a directory of your choice.
3. **Add Path to Windows Environment Variables**:
   - Open the Start Search, type in "env", and select "Edit the system environment variables".
   - Click the "Environment Variables…" button.
   - In the "System variables" section, find and select the "Path" variable, then click "Edit…".
   - Click "New" and add the path to the directory where you extracted Zrok.
   - Click "OK" to save and close all dialogs.

## Usage

4. **Invite Zrok Like User Registration Using CLI**:
```bash
zrok invite
```

Add your email in your CLI, then press Enter. You will receive the Zrok user creation invitation link in your email. Follow the link to create your account.


5. **Login to Zrok Web Portal:**

Go to the settings and click "Enable Your Environment".
Copy the Zrok token.

```bash
zrok enable api_key
```

Paste the token in your terminal to configure Zrok.

6. **Run Your Local Host Port and Configure with Zrok:**

```bash
zrok share public http://127.0.0.1:8000/
```

You will get a Zrok public URL.