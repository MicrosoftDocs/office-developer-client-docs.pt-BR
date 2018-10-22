---
title: Criar um item de contato de um arquivo vCard e salvar o item em uma pasta
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 667278b290e32bc5115a468b1c038d6aa63a5aff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407391"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a><span data-ttu-id="dc416-102">Criar um item de contato de um arquivo vCard e salvar o item em uma pasta</span><span class="sxs-lookup"><span data-stu-id="dc416-102">Create a Contact item from a vCard file and save the item in a folder</span></span>

<span data-ttu-id="dc416-103">Este exemplo importa todos os arquivos vCard em uma pasta do sistema de arquivos e salva os contatos na pasta especificada pelo parâmetro *targetFolder*.</span><span class="sxs-lookup"><span data-stu-id="dc416-103">This example imports all the vCard files in a file system folder and saves the contacts into the folder specified by the *targetFolder* parameter.</span></span>

## <a name="example"></a><span data-ttu-id="dc416-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dc416-104">Example</span></span>

<span data-ttu-id="dc416-105">Este exemplo usa o método [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="dc416-105">This example uses the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method.</span></span> <span data-ttu-id="dc416-106">O método **OpenSharedItem** abre mensagens armazenadas como arquivos de formato de mensagem do Outlook (.msg), arquivos de compromisso iCalendar (.ics) ou arquivos vCard (.vcf).</span><span class="sxs-lookup"><span data-stu-id="dc416-106">The **OpenSharedItem** method opens messages stored as Outlook message format (.msg) files, iCalendar appointment (.ics) files, or vCard (.vcf) files.</span></span> <span data-ttu-id="dc416-107">Certifique-se de converter o objeto retornado no tipo de item apropriado e chame o método **Save** correspondente para persistir o item.</span><span class="sxs-lookup"><span data-stu-id="dc416-107">Be sure to cast the returned object to the appropriate item type and call the corresponding **Save** method to persist the item.</span></span> <span data-ttu-id="dc416-108">Por padrão, o item retornado por **OpenSharedItem** é salvo na pasta padrão para o tipo de item específico.</span><span class="sxs-lookup"><span data-stu-id="dc416-108">By default, the item returned by **OpenSharedItem** is saved in the default folder for the specific item type.</span></span> <span data-ttu-id="dc416-109">Você pode usar o método **Move** correspondente para mover o item para uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="dc416-109">You can use the corresponding **Move** method to move the item to a different folder.</span></span>

<span data-ttu-id="dc416-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dc416-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="dc416-111">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="dc416-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dc416-112">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="dc416-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dc416-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc416-113">See also</span></span>

- [<span data-ttu-id="dc416-114">Contatos</span><span class="sxs-lookup"><span data-stu-id="dc416-114">Contacts</span></span>](contacts.md)

