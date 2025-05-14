# Download UiPath CLI
## Authors
- [Logan Anderson](https://www.linkedin.com/in/logan-anderson-761341165/)

This GitHub Action downloads the specified version of the UiPath Command Line Interface (CLI), making it available for subsequent steps in your workflow. The CLI can be used to analyze or push UiPath projects as part of your CI/CD pipeline.

## 📦 Overview

The UiPath CLI is distributed as a `.nupkg` package from the official UiPath artifacts feed. This action fetches the specified version, extracts it, and adds it to the system path for use in later workflow steps.



## 🚀 Usage

```yaml
name: Download UiPath CLI

on: [push]

jobs:
  download-cli:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Download UiPath CLI
        uses: your-org/download-uipath-cli@v1
        with:
          version: '25.4.9239.19674' # Replace with desired version

      - name: Run UiPath CLI
        run: uipcli help
```

## 🔧 Inputs

| Name     | Description                                   | Required | Default |
|----------|-----------------------------------------------|----------|---------|
| `version` | The version of the UiPath CLI to download.    | ✅ Yes   | N/A     |

**Note:** Available versions can be found at the [UiPath Artifact Feed](https://uipath.visualstudio.com/Public.Feeds/_artifacts/feed/UiPath-Official) by filtering on **UiPath.CLI**.


---

## 👤 Author

**Maintainer:** [Logan Anderson](https://www.linkedin.com/in/logan-anderson-761341165/)

For feedback, questions, or contributions, please open an issue or submit a pull request on the [GitHub repository](https://github.com/UiPath-Logan-COE/Download-UiPath-CLI).
