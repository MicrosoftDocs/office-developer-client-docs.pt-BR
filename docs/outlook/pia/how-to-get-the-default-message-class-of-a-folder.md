---
title: Obter a classe de mensagem padrão de uma pasta
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c03e0737a3dd2e74f39d90ffbac31bb134d16348
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407216"
---
# <a name="get-the-default-message-class-of-a-folder"></a>Obter a classe de mensagem padrão de uma pasta

Este exemplo mostra como usar a propriedade [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obter a classe de mensagens padrão de uma pasta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para obter a classe de mensagem padrão para uma pasta, use a propriedade **DefaultMessageClass** do objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)). Por exemplo, um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) com **DefaultMessageClass** de IPM.Contact significa que ele representa uma pasta Contact. No entanto, se a pasta tiver um formulário personalizado ou um formulário de substituição como um formulário padrão, você deverá usar o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para determinar a classe da mensagem do formulário padrão. A propriedade **DefaultMessageClass** não retorna a classe de mensagem do formulário padrão da pasta.

No exemplo de código a seguir, o procedimento GetDefaultMessageClass usa o **PropertyAccessor** para determinar o formulário padrão de uma pasta. Se a propriedade da pasta **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) não for encontrada e o Outlook gerar um erro, o bloco **try…catch** retorna a propriedade **DefaultMessageClass** para **Folder**.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>Confira também

- [Pastas](folders.md)
