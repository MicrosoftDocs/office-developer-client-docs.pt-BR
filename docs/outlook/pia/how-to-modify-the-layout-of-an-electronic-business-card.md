---
title: Modificar o layout de um cartão de visita eletrônico
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320178"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="6a1e0-102">Modificar o layout de um cartão de visita eletrônico</span><span class="sxs-lookup"><span data-stu-id="6a1e0-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="6a1e0-103">Este exemplo mostra como modificar o layout de um cartão de visita eletrônico usando a propriedade [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) da interface [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6a1e0-103">This example shows how to modify the layout of an electronic business card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="6a1e0-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6a1e0-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6a1e0-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6a1e0-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6a1e0-106">Um cartão de visita eletrônico fornece uma visualização do contato que captura informações específicas desse contato.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-106">An electronic business card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="6a1e0-107">A interface **ContactItem** fornece membros específicos que pertencem a cartões de visita eletrônicos.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-107">The **ContactItem** interface provides specific members that pertain to electronic business cards.</span></span> <span data-ttu-id="6a1e0-108">Estes membros são **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) e [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6a1e0-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)), and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span></span>

<span data-ttu-id="6a1e0-109">No exemplo de código a seguir, BusinessCardLayoutExample modifica o layout de um cartão de visita eletrônico ao receber primeiro um objeto **ContactItem** especificado.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-109">In the following code example, BusinessCardLayoutExample modifies the layout of an electronic business card by first obtaining a specified **ContactItem** object.</span></span> <span data-ttu-id="6a1e0-110">Nesse caso, o **ContactItem** é um contato que tem o valor da propriedade [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) igual a "Melissa MacBeth".</span><span class="sxs-lookup"><span data-stu-id="6a1e0-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to “Melissa MacBeth”.</span></span> <span data-ttu-id="6a1e0-111">Em seguida, BusinessCardLayoutExample cria uma classe de documentos XML [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) e recebe o atributo do layout dessa classe em uma cadeia de caracteres usando o valor **BusinessCardLayoutXML** para o objeto **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-111">Next, BusinessCardLayoutExample creates an XML document class [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k), and then gets the layout attribute of this class in a string by using the **BusinessCardLayoutXML** value for the **ContactItem** object.</span></span> <span data-ttu-id="6a1e0-112">Em seguida, o layout do cartão é alterado de alinhado à esquerda para alinhado à direita.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="6a1e0-113">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6a1e0-114">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6a1e0-115">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="6a1e0-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="6a1e0-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a1e0-116">See also</span></span>

- [<span data-ttu-id="6a1e0-117">Cartões de visita eletrônicos</span><span class="sxs-lookup"><span data-stu-id="6a1e0-117">Electronic business cards</span></span>](electronic-business-cards.md)

