# Auto Firmware Dumper

Automate ROM dumps creation using GitHub Actions with ease. This workflow leverages [DumprX](https://github.com/DumprX/DumprX) to extract firmware and optionally generate device trees compatible with LineageOS, TWRP, and vendor trees.

---

## Supported Languages

- English (this README)
- [简体中文](./README_CN.md)

---

## Requirements

- A valid Stock ROM download link  
  (Supported sources: MediaFire, Mega.nz, Google Drive, AndroidFileHost, or any direct download URL)
- A GitHub Personal Access Token (PAT) with repository permissions
- Patience — firmware dumping can take some time depending on ROM size and network speed

---

## Getting Started

### Step 1: Generate a GitHub Personal Access Token (PAT)

1. Go to your GitHub **Settings > Developer settings > Personal access tokens**.
2. Click **Generate new token (classic)**.
3. Select **repo** scope and all necessary permissions.
4. Generate and **copy the token immediately** — you won't be able to see it again!

### Step 2: Fork This Repository

Fork this repository into your GitHub account to run the workflow.

### Step 3: Configure Repository Secrets

1. Navigate to your forked repository’s **Settings > Secrets and variables > Actions**.
2. Click **New repository secret**.
3. Add a secret named:  
   `GTOKEN`  
   And paste your GitHub Personal Access Token as the value.
4. Save the secret.

### Step 4: Enable GitHub Actions

Make sure Actions are enabled in your repository under **Settings > Actions**.

### Step 5: Run the Workflow

1. Go to the **Actions** tab.
2. Select **Auto Firmware Dumper** workflow.
3. Click **Run workflow**.
4. Fill in the requested inputs:
   - Your GitHub username and email
   - Stock ROM download URL
   - Options to generate and upload Vendor, LineageOS, or TWRP device trees.
5. Start the workflow.

---

## Output

Once completed, your GitHub account will have new repositories named like:

- `dump_<brand>_<device>` – Firmware dump repository
- `android_vendor_<brand>_<device>` – Vendor tree (if enabled)
- `lineage_device_<brand>_<device>` – LineageOS device tree (if enabled)
- `twrp_device_<brand>_<device>` – TWRP device tree (if enabled)

---

## Notes & Tips

- The project is licensed under the [Eclipse Public License 2.0](https://www.eclipse.org/legal/epl-2.0/).
- Dump quality depends on the stock ROM; issues might stem from the source ROM.
- Please use **lowercase letters** for device codenames to avoid errors.
- Files larger than 50MB are automatically deleted due to GitHub size limits.
- Make sure all inputs are filled correctly.
- Select the appropriate checkboxes for generating and uploading device trees.
- If any errors occur or you find bugs, please open an issue.

---

## Support & Contributions

Feel free to open issues or submit pull requests. Your feedback and contributions are highly appreciated.

---

## Developer

**t**  
Email: frnbuid2005@gmail.com  
GitHub: [github.com/t](https://github.com/t)

---

Happy dumping! 
