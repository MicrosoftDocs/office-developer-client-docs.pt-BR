---
title: Exibir na caixa de diálogo Selecionar Nomes no catálogo de endereços que corresponde a uma pasta Contatos
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3be678b13738fead1509f3854c7b23bd0cfc8528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356396"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a><span data-ttu-id="f3c4f-102">Exibir na caixa de diálogo Selecionar Nomes no catálogo de endereços que corresponde a uma pasta Contatos</span><span class="sxs-lookup"><span data-stu-id="f3c4f-102">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>

<span data-ttu-id="f3c4f-103">Este exemplo mostra como obter o catálogo de endereços que corresponde à pasta Contatos padrão e exibe o catálogo de endereços na caixa de diálogo **Selecionar Nomes**.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-103">This example shows how to obtain the address book that corresponds to the default Contacts folder, and then displays the address book in the **Select Names** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="f3c4f-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f3c4f-104">Example</span></span>

<span data-ttu-id="f3c4f-105">Todos os catálogos de endereços no Outlook são representados como um conjunto pela propriedade [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f3c4f-105">All address books in Outlook are represented as a collection by the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="f3c4f-106">O exemplo de código usa o método [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) do objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) para localizar a pasta de contatos que corresponde a cada lista de endereços.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-106">The code sample uses the [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) method of the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object to find the contact folder that corresponds to each address list.</span></span> <span data-ttu-id="f3c4f-107">Cada pasta do Outlook possui uma ID de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-107">Each Outlook folder has an Entry ID.</span></span> <span data-ttu-id="f3c4f-108">Compare a ID de Entrada da pasta Contatos padrão com a ID de Entrada de uma pasta Contatos para produzir a ListaDeEndereços que corresponde à pasta Contatos padrão.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-108">Compare the Entry ID of the default Contacts folder with the Entry ID of a Contacts folder to produce the AddressList that corresponds to the default Contacts folder.</span></span>

<span data-ttu-id="f3c4f-109">Antes de exibir a lista de endereços correspondente à pasta Contatos padrão na caixa de diálogo **Selecionar Nomes**, o exemplo de código a define como o valor da propriedade [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) do objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f3c4f-109">Before displaying the address list corresponding to the default Contacts folder in the **Select Names** dialog box, the code sample sets it as the value of the [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) property of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span>

<span data-ttu-id="f3c4f-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f3c4f-111">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f3c4f-112">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="f3c4f-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f3c4f-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3c4f-113">See also</span></span>

- [<span data-ttu-id="f3c4f-114">Catálogo de Endereços</span><span class="sxs-lookup"><span data-stu-id="f3c4f-114">Address book</span></span>](address-book.md)

