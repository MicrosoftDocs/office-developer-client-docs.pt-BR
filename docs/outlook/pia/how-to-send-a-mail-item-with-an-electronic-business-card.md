---
title: Enviar um item de email com um cartão de visita eletrônico
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25809fc0d1726c9f56be417ae53fadecc831d62f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704543"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a><span data-ttu-id="918ed-102">Enviar um item de email com um cartão de visita eletrônico</span><span class="sxs-lookup"><span data-stu-id="918ed-102">Send a mail item with an electronic business card</span></span>

<span data-ttu-id="918ed-103">Este exemplo cria um item de email, procura um cartão de visita eletrônico e, se encontrar, insere o cartão de visita eletrônico no item de email.</span><span class="sxs-lookup"><span data-stu-id="918ed-103">This example creates a mail item, looks for an electronic business card, and if it finds one, inserts the electronic business card into the mail item.</span></span>

## <a name="example"></a><span data-ttu-id="918ed-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="918ed-104">Example</span></span>

<span data-ttu-id="918ed-105">Para inserir um cartão de visita eletrônico, você pode chamar [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) no objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="918ed-105">To insert an electronic business card, you can call [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) on the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="918ed-106">Esse método obtém uma cadeia de caracteres que representa um endereço de email e tenta localizar um [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) com esse endereço na pasta padrão Contacts.</span><span class="sxs-lookup"><span data-stu-id="918ed-106">This method takes a string representing an email address and attempts to find a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) with that address in the default Contacts folder.</span></span> <span data-ttu-id="918ed-107">Um **ContactItem** pode ter até três endereços de email.</span><span class="sxs-lookup"><span data-stu-id="918ed-107">A **ContactItem** can have as many as three email addresses.</span></span> <span data-ttu-id="918ed-108">Se o contato for encontrado, o exemplo chamará o método **AddBusinessCard** e exibirá a mensagem para o usuário.</span><span class="sxs-lookup"><span data-stu-id="918ed-108">If the contact is found, the example calls the **AddBusinessCard** method, and then displays the message to the user.</span></span>

<span data-ttu-id="918ed-109">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="918ed-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="918ed-110">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="918ed-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="918ed-111">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="918ed-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub AddBusinessCard(ByVal eMailAddress As String)
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML
    Dim contact As Outlook.ContactItem = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find( _
        "[Email1Address]='" & eMailAddress & "'" & " OR " & _
        "[Email2Address]='" & eMailAddress & "'" + " OR " & _
        "[Email3Address]='" & eMailAddress & "'") _
        , Outlook.ContactItem)
    If (contact Is Nothing) Then
        Return
    End If
    mail.AddBusinessCard(contact)
    mail.Display(False)
End Sub
```


```csharp
private void AddBusinessCard(string eMailAddress)
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML;
    Outlook.ContactItem contact = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Email1Address]='" + eMailAddress + "'" + " OR " +
        "[Email2Address]='" + eMailAddress + "'" + " OR " +
        "[Email3Address]='" + eMailAddress + "'")
        as Outlook.ContactItem;
    if (contact == null)
    {
        return;
    }
    mail.AddBusinessCard(contact);
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="918ed-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="918ed-112">See also</span></span>

- [<span data-ttu-id="918ed-113">Cartões de visita eletrônicos</span><span class="sxs-lookup"><span data-stu-id="918ed-113">Electronic business cards</span></span>](electronic-business-cards.md)

