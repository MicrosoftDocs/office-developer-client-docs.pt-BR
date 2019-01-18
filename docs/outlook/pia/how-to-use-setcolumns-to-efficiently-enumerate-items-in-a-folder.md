---
title: Usar SetColumns para enumerar itens de forma eficiente em uma pasta
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708085"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>Usar SetColumns para enumerar itens de forma eficiente em uma pasta

Este exemplo mostra como melhorar o desempenho da enumeração do conjunto [Itens](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) usando o método [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) para armazenar em cache determinadas propriedades de cada item no conjunto.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Para enumerar itens em uma coleção, use o método **SetColumns** para armazenar em cache as propriedades na coleção **Items**. **SetColumns** recebe um argumento que é uma cadeia de caracteres delimitada por vírgula que representa os nomes das propriedades. Depois que todos os itens da coleção tiverem sido enumerados, chame o método [ResetColumns ()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) para limpar o cache de propriedades.

No exemplo de código a seguir, EnumerateContactsWithSetColumns usa o método **SetColumns** para armazenar em cache as propriedades [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) e [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) dos itens na pasta Contatos. Observe que você deve fazer testes em busca de cadeias de caracteres vazias ou uma referência nula na restrição.

Observe que uma pasta do Outlook pode conter itens de tipos diferentes. Esta amostra de código faz uso da classe auxiliar OutlookItem, definida em [Criar uma classe auxiliar para acessar membros comuns de itens do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), para chamar convenientemente a propriedade OutlookItem.Class para verificar a classe de mensagem de cada item no subconjunto filtrado de itens na pasta, antes de definir o item como um item de contato.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

