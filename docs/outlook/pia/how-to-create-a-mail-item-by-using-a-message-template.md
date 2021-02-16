---
title: Criar um item de email usando um modelo de mensagem
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cdd9654187685ceab1062fb4ae1882b2d48c68d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349536"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a><span data-ttu-id="5de8b-102">Criar um item de email usando um modelo de mensagem</span><span class="sxs-lookup"><span data-stu-id="5de8b-102">Create a mail item by using a message template</span></span>

<span data-ttu-id="5de8b-103">Este exemplo cria um item de email usando o método [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5de8b-103">This example creates a mail item by using the [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="5de8b-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5de8b-104">Example</span></span>

<span data-ttu-id="5de8b-105">Este exemplo de código abre o arquivo de modelo Ivy.oft, atribui um assunto e salva a mensagem na pasta Rascunhos.</span><span class="sxs-lookup"><span data-stu-id="5de8b-105">This code sample opens the Ivy.oft template file, assigns a subject, and then saves the message to the Drafts folder.</span></span>

<span data-ttu-id="5de8b-106">O método **CreateItemFromTemplate** será útil se você tiver um arquivo de modelo de formulário do Outlook (.oft) armazenado no disco que você deseja usar como um modelo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5de8b-106">The **CreateItemFromTemplate** method is useful if you have an Outlook form template file (.oft) stored on disk that you want to use as a message template.</span></span> <span data-ttu-id="5de8b-107">O arquivo de modelo pode conter texto pré-formatado, papel de carta ou imagens que você deseja incluir na mensagem.</span><span class="sxs-lookup"><span data-stu-id="5de8b-107">The template file can contain preformatted text, stationery, or images that you want to include in the message.</span></span> <span data-ttu-id="5de8b-108">No entanto, se o arquivo de modelo contiver código por trás do formulário, esse código não será executado.</span><span class="sxs-lookup"><span data-stu-id="5de8b-108">However, if the template file contains code behind the form, the form code will not run.</span></span>

<span data-ttu-id="5de8b-109">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5de8b-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5de8b-110">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="5de8b-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5de8b-111">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="5de8b-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="5de8b-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="5de8b-112">See also</span></span>

- [<span data-ttu-id="5de8b-113">Email</span><span class="sxs-lookup"><span data-stu-id="5de8b-113">Mail</span></span>](mail.md)

