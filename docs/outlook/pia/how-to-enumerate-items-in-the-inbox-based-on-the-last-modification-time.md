---
title: Enumerar itens na Caixa de Entrada com base na hora da última modificação
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320353"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>Enumerar itens na Caixa de Entrada baseada na hora da última modificação

Este exemplo mostra como enumerar itens na pasta Caixa de Entrada com base na hora da última modificação.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Para obter uma **Table**, chame o método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) em um objeto **Folder** ou **Search**. Cada item na **Table** retornada contém apenas um subconjunto padrão das propriedades do item. Cada objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) pode ser considerado como um item na pasta, e cada objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) como uma propriedade de um item. Não há suporte para remover, adicionar ou alterar linhas em **Table**. Para enumerar itens em uma **Table**, use a propriedade [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) para ver se sua posição atual está no fim da tabela. Se **EndOfTable** retornar **false**, use o método [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) para retornar uma **Row**, que contém um número padrão de objetos **Column**. Continue a iteração de forma ininterrupta por meio de **Table ** chamando **GetNextRow** até **EndOfTable** retornar **true**.

No exemplo de código a seguir, DemoTableForInbox obtém um objeto **Table** para a pasta Caixa de Entrada, classifica o objeto **Table** usando a propriedade **LastModificationTime** e o método [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)), iterando a tabela para escrever o assunto de cada item para o rastreamento de assunto de cada item para os ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

