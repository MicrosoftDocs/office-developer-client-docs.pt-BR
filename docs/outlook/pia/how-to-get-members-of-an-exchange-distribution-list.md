---
title: Obter membros de uma lista de distribuição do Exchange
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 730ef62b6bff9cbfc2bf4aaae51116d2fe026131
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406558"
---
# <a name="get-members-of-an-exchange-distribution-list"></a><span data-ttu-id="c4243-102">Obter membros de uma lista de distribuição do Exchange</span><span class="sxs-lookup"><span data-stu-id="c4243-102">Get members of an Exchange distribution list</span></span>

<span data-ttu-id="c4243-103">Este exemplo solicita que o usuário escolha uma lista de distribuição do Exchange na caixa de diálogo **Selecionar Nomes** e expanda a lista de distribuição para exibir seus membros.</span><span class="sxs-lookup"><span data-stu-id="c4243-103">This example prompts the user to select an Exchange distribution list from the **Select Names** dialog box and expands the distribution list to display its members.</span></span>

## <a name="example"></a><span data-ttu-id="c4243-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c4243-104">Example</span></span>

<span data-ttu-id="c4243-105">Esse exemplo de código chama o método [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) do objeto [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) para receber um conjunto [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) que contém todos os membros da lista.</span><span class="sxs-lookup"><span data-stu-id="c4243-105">This code sample calls the [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) method of the [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that contains all the members of the list.</span></span> <span data-ttu-id="c4243-106">Como as listas de distribuição podem ser aninhadas em outra lista de distribuição, o conjunto **AddressEntries** retornado pode representar qualquer tipo de objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) do Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4243-106">Because distribution lists can be nested inside another distribution list, the returned **AddressEntries** collection can represent any type of Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span>


> [!NOTE]
> <span data-ttu-id="c4243-107">A expansão das listas de distribuição pode criar uma carga de desempenho em um servidor Exchange, portanto, use o método **GetExchangeDistributionListMembers** com cautela.</span><span class="sxs-lookup"><span data-stu-id="c4243-107">Expanding distribution lists can create a performance burden on an Exchange server, so use the **GetExchangeDistributionListMembers** method cautiously.</span></span> <span data-ttu-id="c4243-108">Ao expandir grandes listas de distribuição, é normal que seu código fique lento.</span><span class="sxs-lookup"><span data-stu-id="c4243-108">Expect that your code will be slow when it expands large distribution lists.</span></span>

<span data-ttu-id="c4243-109">Para ver os membros de uma lista de distribuição, o usuário deve estar online e conectado a um servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4243-109">To obtain the members of a distribution list, the user must be connected to an Exchange server and online.</span></span>

<span data-ttu-id="c4243-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c4243-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="c4243-111">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="c4243-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c4243-112">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="c4243-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetDistributionListMembers()
    Dim snd As Outlook.SelectNamesDialog = _
        Application.Session.GetSelectNamesDialog()
    Dim addrLists As Outlook.AddressLists = _
        Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        If addrList.Name = "All Groups" Then
            snd.InitialAddressList = addrList
            Exit For
        End If
    Next
    snd.NumberOfRecipientSelectors = _
        Outlook.OlRecipientSelectors.olShowTo
    snd.ToLabel = "D/L"
    snd.ShowOnlyInitialAddressList = True
    snd.AllowMultipleSelection = False
    snd.Display()
    If (snd.Recipients.Count > 0) Then
        Dim addrEntry As Outlook.AddressEntry = _
            snd.Recipients(1).AddressEntry
        If (addrEntry.AddressEntryUserType = _
            Outlook.OlAddressEntryUserType. _
            olExchangeDistributionListAddressEntry) Then
            Dim exchDL As Outlook.ExchangeDistributionList = _
                addrEntry.GetExchangeDistributionList()
            Dim addrEntries As Outlook.AddressEntries = _
                exchDL.GetExchangeDistributionListMembers()
            If Not (addrEntries Is Nothing) Then
                For Each exchDLMember As _
                    Outlook.AddressEntry In addrEntries
                    Debug.WriteLine(exchDLMember.Name)
                Next
            End If
         End If
    End If
End Sub
```


```csharp
private void GetDistributionListMembers()
{
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    Outlook.AddressLists addrLists =
        Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        if (addrList.Name == "All Groups")
        {
            snd.InitialAddressList = addrList;
            break;
        }
    }
    snd.NumberOfRecipientSelectors =
        Outlook.OlRecipientSelectors.olShowTo;
    snd.ToLabel = "D/L";
    snd.ShowOnlyInitialAddressList = true;
    snd.AllowMultipleSelection = false;
    snd.Display();
    if (snd.Recipients.Count > 0)
    {
        Outlook.AddressEntry addrEntry =
            snd.Recipients[1].AddressEntry;
        if (addrEntry.AddressEntryUserType ==
            Outlook.OlAddressEntryUserType.
            olExchangeDistributionListAddressEntry)
        {
            Outlook.ExchangeDistributionList exchDL =
                addrEntry.GetExchangeDistributionList();
            Outlook.AddressEntries addrEntries =
                exchDL.GetExchangeDistributionListMembers();
            if (addrEntries != null)
                foreach (Outlook.AddressEntry exchDLMember
                    in addrEntries)
                {
                    Debug.WriteLine(exchDLMember.Name);
                }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="c4243-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4243-113">See also</span></span>

- [<span data-ttu-id="c4243-114">Usuários do Exchange</span><span class="sxs-lookup"><span data-stu-id="c4243-114">Exchange users</span></span>](exchange-users.md)

