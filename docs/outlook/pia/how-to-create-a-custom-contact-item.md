---
title: Criar um item de contato personalizado
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361051"
---
# <a name="create-a-custom-contact-item"></a>Criar um item de contato personalizado

Este exemplo mostra como criar um item de contato personalizado e definir propriedades predefinidas e definidas pelo usuário.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um objeto [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) representa um contato na pasta Contatos e possui mais de 100 propriedades internas, como [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) e [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)). Às vezes, as propriedades internas não são suficientes e você precisa adicionar propriedades personalizadas, o que pode ser feito usando a coleção [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).

No exemplo de código a seguir, CreateCustomItem cria um objeto **ContactItem** personalizado, nomeia-o como "Shoe Store" e chama o método [Add (String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) para adicioná-lo a uma pasta chamada "Shoe Store". CreateCustomItem primeiro obtém a pasta "Shoe Store" usando o método [ GetDefaultFolder (OlDefaultFolders) ](https://msdn.microsoft.com/library/bb646473\(v=office.15\)). A pasta "Shoe Store" é uma subpasta da pasta Contatos padrão. CreateCustomItem define as propriedades **FirstName** e **LastName**, e cria uma propriedade definida pelo usuário ("Shoe Size") usando a coleção **UserProperties**.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a>Confira também

- [Contatos](contacts.md)

