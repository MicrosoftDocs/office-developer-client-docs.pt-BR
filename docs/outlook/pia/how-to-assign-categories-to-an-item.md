---
title: Atribuir categorias a um item
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f8b94d03a1aea447c4dba859659f044d8ec11994
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713293"
---
# <a name="assign-categories-to-an-item"></a>Atribuir categorias a um item

Este exemplo mostra como atribuir categorias a um item usando a propriedade **Categories**.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Para atribuir categorias a um item, use a propriedade **Categories**. Esta amostra de código utiliza a classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.**Categories** sem ter que lançar o item primeiro. A propriedade **Categories** obtém ou define categorias representadas por uma cadeia delimitada por vírgula que pode conter no máximo 255 caracteres. Vírgulas e espaços são usados para separar os valores da categoria. Atribuir uma categoria que não esteja no conjunto [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) fará com que a categoria não exiba uma cor.

No exemplo de código a seguir, AssignCategories cria uma restrição para itens que contêm “ISV” no assunto, primeiro usando uma consulta DAV Searching and Locating (DASL) para filtrar itens na Caixa de Entrada que contenham “ISV” no assunto. Em seguida, AssignCategories percorre os itens filtrados usando a classe **OutlookItem** e, se a cadeia de caracteres retornada por **item.Categories** não for uma referência nula ou já tiver sido atribuída à ISV, a categoria ISV será atribuída ao item.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a>Confira também

- [Categorias de cor](color-categories.md)

