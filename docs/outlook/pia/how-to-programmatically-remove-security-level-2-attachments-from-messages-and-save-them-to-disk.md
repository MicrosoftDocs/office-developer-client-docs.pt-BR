---
title: Remover programaticamente anexos de nível de segurança 2 das mensagens e salvá-los no disco
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 588d1db8ad222462b2648d4fdb85207fd9bdb782
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539259"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>Remover os anexos de nível 2 de segurança de mensagens e salvá-los no disco por programação

Este exemplo mostra como remover os anexos de nível 2 de segurança de mensagens de email e salvá-los em um disco de onde eles possam ser abertos.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O Outlook protege os usuários de código mal-intencionado transportado por meio de anexos de email que contenham determinadas extensões de arquivo como .exe ou .bat. Esses anexos específicos são bloqueados por padrão e identificados como anexos de nível 1. Os anexos de nível 2 têm uma menor probabilidade de conter código mal-intencionado, mas os usuários não conseguirão abrir um anexo de nível 2 diretamente de uma mensagem de email. Um anexo de nível 2 primeiro deve ser salvo em um disco.

Usando o método [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) no objeto [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)), é possível salvar anexos em um disco. No exemplo de código a seguir, RemoveAttachmentsAndSaveToDisk primeiro remove de itens de email em uma pasta todos os anexos de nível 2 que são maiores do que um tamanho específico. Isso é feito enumerando a propriedade [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) de cada objeto **Attachment** no conjunto [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) e removendo as que são iguais a [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)). RemoveAttachmentsAndSaveToDisk salva o anexo removido usando o método **SaveAsFile**.

> [!NOTE] 
> Os conjuntos no Outlook são lineares. Use o operador [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) para referenciar **Attachments**[1] para **Attachments**[n], onde n representa o valor da propriedade [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).
> 
> Não é possível usar uma instrução **foreach** para remover itens em um conjunto. Em vez disso, use um operador **Index** para obter o primeiro item no conjunto e excluí-lo. Use uma instrução **while** para determinar quando é que você exclui o número apropriado de itens no conjunto. Isso garante que a iteração é feita sobre o número correto de itens no conjunto.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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
            + "http://schemas.microsoft.com/mapi/proptag/0x001A001E"
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

## <a name="see-also"></a>Confira também

- [Anexos](attachments.md)

