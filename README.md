# Setup Defect

![license](https://img.shields.io/github/license/DiscreteTom/setup-defect?style=flat-square)
[![release](https://img.shields.io/github/v/release/DiscreteTom/setup-defect?style=flat-square)](https://github.com/DiscreteTom/setup-defect/releases/latest)

This GitHub Action sets up the [defect](https://github.com/DiscreteTom/defect) binary in your workflow.

> [!NOTE]
> This action only supports Linux x86_64 platform for now.

## Usage

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Setup defect
        uses: DiscreteTom/setup-defect@v0.1.0
        with:
          version: "0.3.2"

      - name: Using the defect binary
        env:
          OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}
        run: |
          defect "hello"
```

## [CHANGELOG](./CHANGELOG.md)
