---
title: Modificar o layout de um cartão de visita eletrônico
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-modify-the-layout-of-an-electronic-business-card?redirectedfrom=MSDN
ms:contentKeyID: 55119838
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6da4971883c97bfe1890bbc5e894c09ab665192b
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773691"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modificar o layout de um cartão de visita eletrônico

Este exemplo mostra como modificar o layout de um cartão de visita eletrônico usando a propriedade [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) da interface [ContactItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.contactitem?redirectedfrom=MSDN&view=outlook-pia).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um cartão de visita eletrônico fornece uma visualização do contato que captura informações específicas desse contato. A interface **ContactItem** fornece membros específicos que pertencem a cartões de visita eletrônicos. Estes membros são **BusinessCardLayoutXml**, [BusinessCardType](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.businesscardtype?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_BusinessCardType), [AddBusinessCardLogoPicture(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.addbusinesscardlogopicture?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_AddBusinessCardLogoPicture_System_String_), [ForwardAsBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.forwardasbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ForwardAsBusinessCard), [ResetBusinessCard()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.resetbusinesscard?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ResetBusinessCard), [SaveBusinessCardImage(String)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.savebusinesscardimage?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_SaveBusinessCardImage_System_String_) e [ShowBusinessCardEditor()](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.showbusinesscardeditor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_ShowBusinessCardEditor).

No exemplo de código a seguir, BusinessCardLayoutExample modifica o layout de um cartão de visita eletrônico ao receber primeiro um objeto **ContactItem** especificado. Nesse caso, o **ContactItem** é um contato que tem o valor da propriedade [Subject](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._contactitem.subject?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__ContactItem_Subject) igual a "Melissa MacBeth". Em seguida, BusinessCardLayoutExample cria uma classe de documentos XML [XmlDocument](https://msdn.microsoft.com/library/6kza7w4k) e recebe o atributo do layout dessa classe em uma cadeia de caracteres usando o valor **BusinessCardLayoutXML** para o objeto **ContactItem**. Em seguida, o layout do cartão é alterado de alinhado à esquerda para alinhado à direita.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

