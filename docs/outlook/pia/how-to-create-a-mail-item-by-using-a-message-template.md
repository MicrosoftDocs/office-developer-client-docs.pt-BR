---
title: Criar um item de email usando um modelo de mensagem
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 074a3eb7b83e4556b41549d18b81c97b96db1e6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407097"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>Criar um item de email usando um modelo de mensagem

Este exemplo cria um item de email usando o método [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)).

## <a name="example"></a>Exemplo

Este exemplo de código abre o arquivo de modelo Ivy.oft, atribui um assunto e salva a mensagem na pasta Rascunhos.

O método **CreateItemFromTemplate** será útil se você tiver um arquivo de modelo de formulário do Outlook (.oft) armazenado no disco que você deseja usar como um modelo de mensagem. O arquivo de modelo pode conter texto pré-formatado, papel de carta ou imagens que você deseja incluir na mensagem. No entanto, se o arquivo de modelo contiver código por trás do formulário, esse código não será executado.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.

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

## <a name="see-also"></a>Confira também

- [Email](mail.md)

