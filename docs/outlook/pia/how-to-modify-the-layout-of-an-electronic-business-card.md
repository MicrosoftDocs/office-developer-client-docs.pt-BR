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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722736"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modificar o layout de um cartão de visita eletrônico

Este exemplo mostra como modificar o layout de um cartão de visita eletrônico usando a propriedade [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) da interface [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um cartão de visita eletrônico fornece uma visualização do contato que captura informações específicas desse contato. A interface **ContactItem** fornece membros específicos que pertencem a cartões de visita eletrônicos. Estes membros são **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) e [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).

No exemplo de código a seguir, BusinessCardLayoutExample modifica o layout de um cartão de visita eletrônico ao receber primeiro um objeto **ContactItem** especificado. Nesse caso, o **ContactItem** é um contato que tem o valor da propriedade [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) igual a "Melissa MacBeth". Em seguida, BusinessCardLayoutExample cria uma classe de documentos XML [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k) e recebe o atributo do layout dessa classe em uma cadeia de caracteres usando o valor **BusinessCardLayoutXML** para o objeto **ContactItem**. Em seguida, o layout do cartão é alterado de alinhado à esquerda para alinhado à direita.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Cartões de visita eletrônicos](electronic-business-cards.md)

