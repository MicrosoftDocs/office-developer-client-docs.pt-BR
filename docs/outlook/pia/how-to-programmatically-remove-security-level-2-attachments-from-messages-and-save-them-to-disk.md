---
title: Remover programaticamente anexos de nível de segurança 2 das mensagens e salvá-los no disco
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 135f07f4bd3bdc36cee8547106b955b967150df8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320143"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="949e9-102">Remover os anexos de nível 2 de segurança de mensagens e salvá-los no disco por programação</span><span class="sxs-lookup"><span data-stu-id="949e9-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="949e9-103">Este exemplo mostra como remover os anexos de nível 2 de segurança de mensagens de email e salvá-los em um disco de onde eles possam ser abertos.</span><span class="sxs-lookup"><span data-stu-id="949e9-103">This example shows how to remove security level 2 attachments from email messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="949e9-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="949e9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="949e9-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="949e9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="949e9-106">O Outlook protege os usuários de código mal-intencionado transportado por meio de anexos de email que contenham determinadas extensões de arquivo como .exe ou .bat.</span><span class="sxs-lookup"><span data-stu-id="949e9-106">Outlook protects users from malicious code transported via email attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="949e9-107">Esses anexos específicos são bloqueados por padrão e identificados como anexos de nível 1.</span><span class="sxs-lookup"><span data-stu-id="949e9-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="949e9-108">Os anexos de nível 2 têm uma menor probabilidade de conter código mal-intencionado, mas os usuários não conseguirão abrir um anexo de nível 2 diretamente de uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="949e9-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an email message.</span></span> <span data-ttu-id="949e9-109">Um anexo de nível 2 primeiro deve ser salvo em um disco.</span><span class="sxs-lookup"><span data-stu-id="949e9-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="949e9-110">Usando o método [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) no objeto [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), é possível salvar anexos em um disco.</span><span class="sxs-lookup"><span data-stu-id="949e9-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="949e9-111">No exemplo de código a seguir, RemoveAttachmentsAndSaveToDisk primeiro remove de itens de email em uma pasta todos os anexos de nível 2 que são maiores do que um tamanho específico.</span><span class="sxs-lookup"><span data-stu-id="949e9-111">In the following code example, RemoveAttachmentsAndSaveToDisk first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="949e9-112">Isso é feito enumerando a propriedade [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de cada objeto **Attachment** no conjunto [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) e removendo as que são iguais a [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="949e9-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span></span> <span data-ttu-id="949e9-113">RemoveAttachmentsAndSaveToDisk salva o anexo removido usando o método **SaveAsFile**.</span><span class="sxs-lookup"><span data-stu-id="949e9-113">RemoveAttachmentsAndSaveToDisk then saves the removed attachment by using the **SaveAsFile** method.</span></span>

> [!NOTE] 
> <span data-ttu-id="949e9-114">Os conjuntos no Outlook são lineares.</span><span class="sxs-lookup"><span data-stu-id="949e9-114">Collections in Outlook are linear.</span></span> <span data-ttu-id="949e9-115">Use o operador [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) para referenciar **Attachments**[1] para **Attachments**[n], onde n representa o valor da propriedade [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="949e9-115">Use the [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) operator to reference **Attachments**[1] to **Attachments**[n], where n represents the value of the [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia) property.</span></span>
> 
> <span data-ttu-id="949e9-116">Não é possível usar uma instrução **foreach** para remover itens em um conjunto.</span><span class="sxs-lookup"><span data-stu-id="949e9-116">You cannot use a **foreach** statement to remove items in a collection.</span></span> <span data-ttu-id="949e9-117">Em vez disso, use um operador **Index** para obter o primeiro item no conjunto e excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="949e9-117">Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item.</span></span> <span data-ttu-id="949e9-118">Use uma instrução **while** para determinar quando é que você exclui o número apropriado de itens no conjunto.</span><span class="sxs-lookup"><span data-stu-id="949e9-118">Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection.</span></span> <span data-ttu-id="949e9-119">Isso garante que a iteração é feita sobre o número correto de itens no conjunto.</span><span class="sxs-lookup"><span data-stu-id="949e9-119">This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="949e9-120">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="949e9-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="949e9-121">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="949e9-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="949e9-122">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="949e9-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "https://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="949e9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="949e9-123">See also</span></span>

- [<span data-ttu-id="949e9-124">Anexos</span><span class="sxs-lookup"><span data-stu-id="949e9-124">Attachments</span></span>](attachments.md)

