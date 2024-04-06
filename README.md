# bicep-azcli
Commands:
On Mac: 
Install homebrew: 
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
Error: zsh: command not found: brew
echo 'eval $(/opt/homebrew/bin/brew shellenv)' >> /Users/"YOUR USER NAME"/.zprofile
echo 'eval $(/opt/homebrew/bin/brew shellenv)' >> /Users/"YOUR USER NAME"/.zprofile

Main.bicep:
resource storageAccount 'Microsoft.Storage/storageAccounts@2023-01-01'={
  name: 'teststgtoystg12345'
  location: 'southindia'
  sku: {
    name: 'Standard_LRS'
  }
  kind: 'StorageV2'
  properties: {
    accessTier: 'Hot'
  }
}

Commands:
az login
az configure --defaults group=bicep-rg
az deployment group create --template-file=/main.bicep
az deployment group list -o table      
