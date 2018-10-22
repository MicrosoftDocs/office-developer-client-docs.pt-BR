---
title: Obter a conta de uma pasta
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d83a145b577cbc9be68cdd694f7806da7cdad512
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407202"
---
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="d8afb-102">Obter a conta de uma pasta</span><span class="sxs-lookup"><span data-stu-id="d8afb-102">Get the metadata for a folder.</span></span>

<span data-ttu-id="d8afb-103">Este exemplo obtém a conta associada a uma pasta na sessão atual.</span><span class="sxs-lookup"><span data-stu-id="d8afb-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="d8afb-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8afb-104">Example</span></span>

<span data-ttu-id="d8afb-105">No exemplo de código a seguir, a função DisplayAccountForCurrentFolder chama a função GetAccountForFolder para identificar a conta cujo armazenamento de entrega padrão hospeda a pasta atual e, em seguida, exibe o nome da pasta.</span><span class="sxs-lookup"><span data-stu-id="d8afb-105">In the following code example, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="d8afb-106">GetAccountForFolder corresponde o repositório da pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com o repositório de entrega padrão de cada conta (obtida com a propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) definida na coleção [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) para a sessão.</span><span class="sxs-lookup"><span data-stu-id="d8afb-106">In the following code sample, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.  GetAccountForFolder  matches the store of the current folder (obtained from  the  Folder.Store  property) with the default delivery store of each account (obtained  with the  Account.DeliveryStore  property) that is defined in the Accounts collection for the session. GetAccountForFolder returns the  Account object when a match is found; otherwise it returns null.</span></span> <span data-ttu-id="d8afb-107">GetAccountForFolder retorna o objeto [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) se uma correspondência for encontrada; caso contrário, retorna uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="d8afb-107">GetAccountForFolder returns the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="d8afb-108">Em uma sessão do Microsoft Outlook com várias contas definidas no perfil, a pasta exibida no Explorer ativo não reside necessariamente no repositório padrão dessa sessão; em vez disso, ela pode residir em um dos vários repositórios associados às várias contas.</span><span class="sxs-lookup"><span data-stu-id="d8afb-108">In a outlooknv1 session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span> <span data-ttu-id="d8afb-109">Este tópico mostra como identificar a conta cujo repositório de entrega padrão é o mesmo repositório que hospeda a pasta.</span><span class="sxs-lookup"><span data-stu-id="d8afb-109">This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="d8afb-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d8afb-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="d8afb-111">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="d8afb-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d8afb-112">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="d8afb-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d8afb-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8afb-113">See also</span></span>

- [<span data-ttu-id="d8afb-114">Contas</span><span class="sxs-lookup"><span data-stu-id="d8afb-114">Accounts</span></span>](accounts.md)

