---
title: Criar um item enviável para uma conta específica com base na pasta atual
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ccbbaab10dc88d50c1fad3c1eefeb5c222bc8446
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349529"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="522e7-102">Criar um item enviável para uma conta específica com base na pasta atual</span><span class="sxs-lookup"><span data-stu-id="522e7-102">Create a sendable item for a specific account based on the current folder</span></span>

<span data-ttu-id="522e7-103">Este tópico inclui dois exemplos de código que mostram como criar um item de email e solicitação de reunião enviáveis, e como enviá-los usando uma conta específica baseada na pasta atual.</span><span class="sxs-lookup"><span data-stu-id="522e7-103">This topic contains two code examples that show how to create a sendable email item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="522e7-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="522e7-104">Example</span></span>

<span data-ttu-id="522e7-105">Quando você usa o método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) do objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) para criar um item do Outlook, o item é criado para a conta principal daquela sessão.</span><span class="sxs-lookup"><span data-stu-id="522e7-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create an Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="522e7-106">Em uma sessão com várias contas definidas no perfil, você pode criar um item para uma conta IMAP, POP ou Exchange específica.</span><span class="sxs-lookup"><span data-stu-id="522e7-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Exchange account.</span></span> 

<span data-ttu-id="522e7-107">Se houver várias contas no perfil atual e você criar um item enviável na interface do usuário, por exemplo, clicando em **Novo email** ou **Nova reunião**, um inspetor exibe um novo item de email ou solicitação de reunião no modo Redigir, e você pode então selecionar a conta de onde quer enviar o item.</span><span class="sxs-lookup"><span data-stu-id="522e7-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New Email** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="522e7-108">Este tópico mostra como criar um item enviável programaticamente e enviá-lo usando uma conta de envio específica.</span><span class="sxs-lookup"><span data-stu-id="522e7-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="522e7-109">O tópico tem dois exemplos de código que mostram como criar um [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e um [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) para uma conta específica que é determinada pela pasta atual no explorer ativo.</span><span class="sxs-lookup"><span data-stu-id="522e7-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="522e7-110">Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="522e7-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="522e7-111">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="522e7-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="522e7-112">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="522e7-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="522e7-113">No primeiro método, CreateMailItemFromAccount identifica primeiro a conta apropriada fazendo a correspondência da loja na pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com a loja de entrega padrão de cada conta (obtida com a propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definida na coleção de [Contas](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) da sessão.</span><span class="sxs-lookup"><span data-stu-id="522e7-113">In the first method, CreateMailItemFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="522e7-114">CreateMailItemFromAccount cria o **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="522e7-114">CreateMailItemFromAccount then creates the **MailItem**.</span></span> 

<span data-ttu-id="522e7-115">Para associar o item à conta, CreateMailItemFromAccount designa o usuário da conta como o remetente do item definindo a propriedade account.CurrentUser.AddressEntry para a propriedade [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) do **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="522e7-115">To associate the item with the account, CreateMailItemFromAccount assigns the user of the account as the sender of the item by setting the account.CurrentUser.AddressEntry property to the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem**.</span></span> <span data-ttu-id="522e7-116">A atribuição da propriedade Sender é a etapa importante; se você não especificar o remetente, o **MailItem** é criado para a conta principal por padrão.</span><span class="sxs-lookup"><span data-stu-id="522e7-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="522e7-117">No final do método, CreateMailItemFromAccount exibe o **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="522e7-117">At the end of the method, CreateMailItemFromAccount displays the **MailItem**.</span></span> <span data-ttu-id="522e7-118">Observe que, se a pasta atual não está em uma loja de entrega, CreateMailItemFromAccount cria o **MailItem** para conta principal da sessão.</span><span class="sxs-lookup"><span data-stu-id="522e7-118">Note that if the current folder is not on a delivery store, CreateMailItemFromAccount creates the **MailItem** for the primary account for the session.</span></span>

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

<span data-ttu-id="522e7-119">O próximo método, CreateMeetingRequestFromAccount, é semelhante ao CreateMailItemFromAccount, exceto por criar um AppointmentItem em vez de um MailItem.</span><span class="sxs-lookup"><span data-stu-id="522e7-119">The next method, CreateMeetingRequestFromAccount, is similar to CreateMailItemFromAccount except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="522e7-120">CreateMeetingRequestFromAccount identifica primeiro a conta apropriada fazendo a correspondência da loja da pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com a loja de entrega padrão de cada conta (obtida da propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definida na coleção de Contas da sessão.</span><span class="sxs-lookup"><span data-stu-id="522e7-120">CreateMeetingRequestFromAccount first identifies the appropriate account by matching the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained from the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="522e7-121">CreateMeetingRequestFromAccount cria AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="522e7-121">CreateMeetingRequestFromAccount then creates the AppointmentItem.</span></span> 

<span data-ttu-id="522e7-122">Para associar o item com a conta, CreateMeetingRequestFromAccount designa essa conta como o item da conta de envio, definindo o objeto [Conta](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) do AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="522e7-122">To associate the item with the account, CreateMeetingRequestFromAccount assigns that account as the item's sending account by setting the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to the [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) property of the AppointmentItem.</span></span> <span data-ttu-id="522e7-123">A atribuição da propriedade SendUsingAccount é a etapa importante; se você não especificar o remetente, o AppointmentItem é criado para a conta principal por padrão.</span><span class="sxs-lookup"><span data-stu-id="522e7-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="522e7-124">No final do método, CreateMeetingRequestFromAccount exibe o AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="522e7-124">At the end of the method, CreateMeetingRequestFromAccount displays the AppointmentItem.</span></span> <span data-ttu-id="522e7-125">Observe que, se a pasta atual não está em uma loja de entrega, CreateMeetingRequestFromAccount cria o AppointmentItem para a conta principal da sessão.</span><span class="sxs-lookup"><span data-stu-id="522e7-125">Note that if the current folder is not on a delivery store, CreateMeetingRequestFromAccount creates the AppointmentItem for the primary account for the session.</span></span>

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="522e7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="522e7-126">See also</span></span>

- [<span data-ttu-id="522e7-127">Contas</span><span class="sxs-lookup"><span data-stu-id="522e7-127">Accounts</span></span>](accounts.md)

