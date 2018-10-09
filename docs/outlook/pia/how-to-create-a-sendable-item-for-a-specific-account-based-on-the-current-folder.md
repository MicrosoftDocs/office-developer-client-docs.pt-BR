---
title: Criar um item enviável para uma conta específica com base na pasta atual
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 076677ed2eeedb269ddddc3bee201a162196db0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405760"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>Criar um item enviável para uma conta específica com base na pasta atual

Este tópico inclui dois exemplos de código que mostram como criar um item de email e solicitação de reunião enviáveis, e como enviá-los usando uma conta específica baseada na pasta atual.

## <a name="example"></a>Exemplo

Quando você usa o método [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) do objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) para criar um item do Outlook, o item é criado para a conta principal daquela sessão. Em uma sessão com várias contas definidas no perfil, você pode criar um item para uma conta IMAP, POP ou Exchange específica. 

Se houver várias contas no perfil atual e você criar um item enviável na interface do usuário, por exemplo, clicando em **Novo email** ou **Nova reunião**, um inspetor exibe um novo item de email ou solicitação de reunião no modo Redigir, e você pode então selecionar a conta de onde quer enviar o item. 

Este tópico mostra como criar um item enviável programaticamente e enviá-lo usando uma conta de envio específica. O tópico tem dois exemplos de código que mostram como criar um [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e um [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) para uma conta específica que é determinada pela pasta atual no explorer ativo.

Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

No primeiro método, CreateMailItemFromAccount identifica primeiro a conta apropriada fazendo a correspondência da loja na pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com a loja de entrega padrão de cada conta (obtida com a propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definida na coleção de [Contas](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) da sessão. CreateMailItemFromAccount cria o **MailItem**. 

Para associar o item à conta, CreateMailItemFromAccount designa o usuário da conta como o remetente do item definindo a propriedade account.CurrentUser.AddressEntry para a propriedade [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) do **MailItem**. A atribuição da propriedade Sender é a etapa importante; se você não especificar o remetente, o **MailItem** é criado para a conta principal por padrão. No final do método, CreateMailItemFromAccount exibe o **MailItem**. Observe que, se a pasta atual não está em uma loja de entrega, CreateMailItemFromAccount cria o **MailItem** para conta principal da sessão.

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

O próximo método, CreateMeetingRequestFromAccount, é semelhante ao CreateMailItemFromAccount, exceto por criar um AppointmentItem em vez de um MailItem. CreateMeetingRequestFromAccount identifica primeiro a conta apropriada fazendo a correspondência da loja da pasta atual (obtida da propriedade [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) com a loja de entrega padrão de cada conta (obtida da propriedade [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) que está definida na coleção de Contas da sessão. CreateMeetingRequestFromAccount cria AppointmentItem. 

Para associar o item com a conta, CreateMeetingRequestFromAccount designa essa conta como o item da conta de envio, definindo o objeto [Conta](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) para a propriedade [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) do AppointmentItem. A atribuição da propriedade SendUsingAccount é a etapa importante; se você não especificar o remetente, o AppointmentItem é criado para a conta principal por padrão. No final do método, CreateMeetingRequestFromAccount exibe o AppointmentItem. Observe que, se a pasta atual não está em uma loja de entrega, CreateMeetingRequestFromAccount cria o AppointmentItem para a conta principal da sessão.

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

## <a name="see-also"></a>Confira também

- [Contas](accounts.md)

