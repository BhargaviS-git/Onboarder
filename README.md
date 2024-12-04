# Onboarder
Onboarder Automator


{
  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
  "contentVersion": "1.0.0.0",
  "resources": [
    {
      "type": "Microsoft.Compute/virtualMachines",
      "apiVersion": "2021-03-01",
      "location": "[parameters('location')]",
      "properties": {
        "hardwareProfile": {
          "vmSize": "[parameters('vmSize')]"
        },
        "storageProfile": {
          "osDisk": {
            "createOption": "FromImage",
            "managedDisk": {
              "storageAccountType": "Standard_LRS"
            },
            "image": {
              "uri": "[parameters('imageUri')]"
            }
          }
        },
        "osProfile": {
          "computerName": "[parameters('vmName')]",
          "adminUsername": "[parameters('adminUsername')]",
          "adminPassword": "[parameters('adminPassword')]"
        },
        "networkProfile": {
          "networkInterfaces": [
            {
              "id": "[resourceId('Microsoft.Network/networkInterfaces', parameters('nicName'))]"
            }
          ]
        }
      }
    }
  ],
  "parameters": {
    "location": {
      "type": "string",
      "defaultValue": "eastus"
    },
    "vmSize": {
      "type": "string",
      "defaultValue": "Standard_D2_v2"
    },
    "imageUri": {
      "type": "string",
      "defaultValue": "https://path/to/image.vhd"
    },
    "vmName": {
      "type": "string",
      "defaultValue": "[concat('vm-', parameters('firstName'), '-', parameters('lastName'))]"
    },
    "adminUsername": {
      "type": "string"
    },
    "adminPassword": {
      "type": "string"
    },
    "nicName": {
      "type": "string",
      "defaultValue": "nic-12345"
    }
  }
}
