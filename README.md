# GitHub Actions to deploy ARM Storage Template

Link to sample ARM storage template: https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-storage-account-create/azuredeploy.json

# Step 1 - Générer les informations d'identification du déploiement

Azure CLI: 

<b>az ad sp create-for-rbac --name {myApp} --role contributor --scopes /subscriptions/{subscription-id}/resourceGroups/{MyResourceGroup} --sdk-auth</b>

# Step 2 - Creer les secrets dans le repo GitHub

a/ Copier l'output de la commande ci-dessus dans un secret GitHub <b>AZURE_CREDENTIALS</b>

{<br>
  "clientId": "<GUID>",<br>
  "clientSecret": "<GUID>",<br>
  "subscriptionId": "<GUID>",<br>
  "tenantId": "<GUID>",<br>
  (...)<br>
}<br>
<br>
  
b/ Créer un 2nd secret <b>AZURE_SUBID</b> contenant l'ID de la souscription Azure

# Step 3 - Creer un dossier ARM

Déposer le template et le fichier de paramètre ARM à l'intérieur

# Step 4 - Modeliser le workflow GitHub Actions

Créer un dossier .github/workflows à la racine du repository
Créer un fichier workflow.yml à l'intérieur pour coder le workflow
