---
title: Obter a classe de mensagem padrão de uma pasta
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 031b7736ed397b9218ea677442f80595da2aa919
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542559"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="73fe1-102">Obter a classe de mensagem padrão de uma pasta</span><span class="sxs-lookup"><span data-stu-id="73fe1-102">Get the default message class of a folder</span></span>

<span data-ttu-id="73fe1-103">Este exemplo mostra como usar a propriedade [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) para obter a classe de mensagens padrão de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="73fe1-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="73fe1-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="73fe1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="73fe1-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="73fe1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="73fe1-106">Para obter a classe de mensagem padrão para uma pasta, use a propriedade **DefaultMessageClass** do objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="73fe1-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="73fe1-107">Por exemplo, um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) com **DefaultMessageClass** de IPM.Contact significa que ele representa uma pasta Contact.</span><span class="sxs-lookup"><span data-stu-id="73fe1-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="73fe1-108">No entanto, se a pasta tiver um formulário personalizado ou um formulário de substituição como um formulário padrão, você deverá usar o objeto [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) para determinar a classe da mensagem do formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="73fe1-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="73fe1-109">A propriedade **DefaultMessageClass** não retorna a classe de mensagem do formulário padrão da pasta.</span><span class="sxs-lookup"><span data-stu-id="73fe1-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="73fe1-110">No exemplo de código a seguir, o procedimento GetDefaultMessageClass usa o **PropertyAccessor** para determinar o formulário padrão de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="73fe1-110">In the following code example, the GetDefaultMessageClass procedure uses the **PropertyAccessor** to determine the default form of a folder.</span></span> <span data-ttu-id="73fe1-111">Se a propriedade de pasta **PR \_ DEF \_ POST \_ MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) não for encontrada e o Outlook criar um erro, **tente... catch** block returns the **DefaultMessageClass** property for the **Folder**.</span><span class="sxs-lookup"><span data-stu-id="73fe1-111">If the folder property **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) is not found and Outlook raises an error, the **try…catch** block returns the **DefaultMessageClass** property for the **Folder**.</span></span>

<span data-ttu-id="73fe1-112">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="73fe1-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="73fe1-113">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="73fe1-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="73fe1-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="73fe1-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
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

## <a name="see-also"></a><span data-ttu-id="73fe1-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="73fe1-115">See also</span></span>

- [<span data-ttu-id="73fe1-116">Pastas</span><span class="sxs-lookup"><span data-stu-id="73fe1-116">Folders</span></span>](folders.md)

