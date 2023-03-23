# Algolia Upload Records
Upload query data records to Algolia

## Set Secrets
`Settings => Secrets => New repository secret`

[![pptH7f1.jpg](https://s1.ax1x.com/2023/03/20/pptH7f1.jpg)](https://imgse.com/i/pptH7f1)



## Example usage
```bash
# Use Algolia Upload Records action
uses: feiflown/Algolia-Upload-Records@main
# Set environment variables
env:
  APPLICATION_ID: ${{secrets.APPLICATION_ID}}
  ADMIN_API_KEY: ${{secrets.ADMIN_API_KEY}}
  INDEX_NAME: ${{secrets.INDEX_NAME}}
  FILE_PATH: ${{secrets.FILE_PATH}}
```

## Full example usage
```bash
name: Algolia Upload Records

on:
  [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Upload Records
        uses: feiflown/Algolia-Upload-Records@main
        env:
          APPLICATION_ID: ${{secrets.APPLICATION_ID}}
          ADMIN_API_KEY: ${{secrets.ADMIN_API_KEY}}
          INDEX_NAME: ${{secrets.INDEX_NAME}}
          FILE_PATH: ${{secrets.FILE_PATH}}
```

## Example
[使用 GitHub Action 自动上传搜索记录到 Algolia](https://feiflown.github.io/post/algolia-auto-update/)

