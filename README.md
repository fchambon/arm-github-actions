# GitHub Actions to deploy ARM Storage Template

Link to sample ARM storage template: https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/101-storage-account-create/azuredeploy.json

# Step 1 - Générer les informations d'identification du déploiement

Azure CLI: 

az ad sp create-for-rbac --name {myApp} --role contributor --scopes /subscriptions/{subscription-id}/resourceGroups/{MyResourceGroup} --sdk-auth



