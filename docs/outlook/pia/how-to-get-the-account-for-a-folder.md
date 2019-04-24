---
title: Obter a conta de uma pasta
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320213"
---
# <a name="get-the-account-for-a-folder"></a>Obter a conta de uma pasta

Este exemplo obtém a conta associada a uma pasta na sessão atual.

## <a name="example"></a>Exemplo

No exemplo de código a seguir, a função DisplayAccountForCurrentFolder chama a função GetAccountForFolder para identificar a conta cujo armazenamento de entrega padrão hospeda a pasta atual e, em seguida, exibe o nome da pasta. GetAccountForFolder corresponde o repositório da pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com o repositório de entrega padrão de cada conta (obtida com a propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) definida na coleção [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para a sessão. GetAccountForFolder retorna o objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) se uma correspondência for encontrada; caso contrário, retorna uma referência nula.

Em uma sessão do Microsoft Outlook com várias contas definidas no perfil, a pasta exibida no Explorer ativo não reside necessariamente no repositório padrão dessa sessão; em vez disso, ela pode residir em um dos vários repositórios associados às várias contas. Este tópico mostra como identificar a conta cujo repositório de entrega padrão é o mesmo repositório que hospeda a pasta.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a>Confira também

- [Contas](accounts.md)

