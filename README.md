# Obfuscate with PSU

This is a GitHub action that allows you to integrate PSU obfuscation into your pipeline.

### Prerequisites
- A PSU Premium subscription
- Your API key
- Your Lua script to be obfuscated

### Known Caveats
Multiple files cannot be obfuscated at once at this time - this issue will be addressed in a later release of the action.

# Usage

### Prerequisites
Create a workflow `.yml` file in `.github/workflows` inside of your repository. An example workflow can be found below.

### Inputs
- `file` - The path to the file to be obfuscated
- `apiKey` - Your PSU API key, this can be specified through GitHub's secrets.

### Outputs
- `file` - The obfuscated file

### Example workflow
```yml
name: Example Workflow
on: push

jobs:
  obfuscate:
    runs-on: ubuntu-latest

    steps:
    - uses: psuDevelopment/Obfuscate-With-PSU@v1.0.0-BETA
      id: file
      with:
        file: MyAwesomeScript.lua
        apiKey: ${{ secrets.PSU_API_KEY }}
```

# Licensing

This project is licensed under the MIT license, feel free to modify as you wish. :)
