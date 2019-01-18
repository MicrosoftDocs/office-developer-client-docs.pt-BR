---
title: Criar uma lista de distribuição
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721756"
---
# <a name="create-a-distribution-list"></a>Criar uma lista de distribuição

Este exemplo mostra como criar uma lista de distribuição e exibi-la ao usuário.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


No exemplo de código a seguir, CreateDistributionList cria uma lista de distribuição chamando o método [CreateItem (OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) para criar um objeto [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)). Em seguida, ele cria um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) e chama o método [GetTable (Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) para localizar todos os contatos na pasta Contatos padrão para os quais o valor da propriedade [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) é "Top Customer" e o valor da propriedade [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) não está vazio. Depois que todos os contatos são identificados, o nome **Email1Address** é adicionado como uma coluna à **Table**. CreateDistributionList cria um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) usando o método [CreateRecipient (String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). CreateDistributionList finalmente exibe a lista de distribuição "Top Customers" para o usuário.

> [!NOTE] 
> Você deve passar um objeto **Recipient** resolvido como um parâmetro para o método [AddMember (Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) do objeto [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)). Para resolver um objeto **Recipient**, use o método [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>Confira também

- [Usuários do Exchange](exchange-users.md)

