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
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Exibir na caixa de diálogo Selecionar Nomes no catálogo de endereços que corresponde a uma pasta Contatos

Este exemplo mostra como obter o catálogo de endereços que corresponde à pasta Contatos padrão e exibe o catálogo de endereços na caixa de diálogo **Selecionar Nomes**.

## <a name="example"></a>Exemplo

Todos os catálogos de endereços no Outlook são representados como um conjunto pela propriedade [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). O exemplo de código usa o método [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) do objeto [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) para localizar a pasta de contatos que corresponde a cada lista de endereços. Cada pasta do Outlook possui uma ID de entrada. Compare a ID de Entrada da pasta Contatos padrão com a ID de Entrada de uma pasta Contatos para produzir a ListaDeEndereços que corresponde à pasta Contatos padrão.

Antes de exibir a lista de endereços correspondente à pasta Contatos padrão na caixa de diálogo **Selecionar Nomes**, o exemplo de código a define como o valor da propriedade [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) do objeto [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.

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

## <a name="see-also"></a>Confira também

- [Catálogo de Endereços](address-book.md)

