---
title: Filtrar e exibir itens da Caixa de entrada modificados no último mês
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77fe6e7df4cf67ed1ca2d62b8cf48f1b2873ccbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320290"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>Filtro e exibir os itens de caixa de entrada modificados no mês passado

Este exemplo mostra como filtrar e exibir os itens de caixa de entrada que foram modificados no mês passado.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

A linguagem de consulta DAV Searching and Locating (DASL) se baseia na implementação do Microsoft Exchange do DASL no Outlook. Pode ser usada para retornar resultados com base em propriedades para pesquisas em nível de item nos dados de pastas, como os representados por um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). Os filtros DASL suportam comparações de cadeias de caracteres, incluindo equivalência, prefixo, frase e correspondência de subcadeias, usando o operado igual (=). É possível usar consultas DASL para executar comparações e filtragens de data-hora.

Como as consultas DASL sempre executam comparações **DateTime** em Tempo Universal Coordenado (UTC), é necessário converter o valor da hora local para UTC para que a consulta funcione corretamente. Você também deve converter o valor de **DateTime** em uma representação de cadeia de caracteres, pois os filtros DASL suportam comparações de cadeias. Você pode fazer a conversão **Date Time** de duas maneiras: usando o método [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) do objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)), ou usando as macros **DateTime**do Outlook para fazer a conversão.

A seguinte linha de código mostra como usar o método**LocalTimeToUTC** para converter o valor da propriedade **LastModificationTime** (que é uma coluna padrão em todos os objetos **Item**) para UTC.

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

A tabela seguinte lista as macros **DateTime** que você pode usar para retornar cadeias de caracteres filtradas que comparam o valor de uma propriedade **DateTime** determinada com uma data relativa especificada ou com um intervalo de datas em UTC. O valor de propriedade SchemaName representa um qualquer propriedade **DateTime** válida referenciada por namespace.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Macro</p></th>
<th><p>Sintaxe</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>today</p></td>
<td><p>%today(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valor de propriedade SchemaName igual a hoje.</p></td>
</tr>
<tr class="even">
<td><p>tomorrow</p></td>
<td><p>%tomorrow(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valor de propriedade SchemaName igual a amanhã.</p></td>
</tr>
<tr class="odd">
<td><p>yesterday</p></td>
<td><p>%yesterday(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valor de propriedade SchemaName igual a ontem.</p></td>
</tr>
<tr class="even">
<td><p>next7days</p></td>
<td><p>%next7days(“SchemaName”)%</p></td>
<td><p>Restringir aos itens com valores de propriedade SchemaName em um intervalo equivalente aos próximos sete dias.</p></td>
</tr>
<tr class="odd">
<td><p>last7days</p></td>
<td><p>%last7days(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente aos últimos sete dias.</p></td>
</tr>
<tr class="even">
<td><p>nextweek</p></td>
<td><p>%nextweek(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente à próxima semana.</p></td>
</tr>
<tr class="odd">
<td><p>thisweek</p></td>
<td><p>%thisweek(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente a esta semana.</p></td>
</tr>
<tr class="even">
<td><p>lastweek</p></td>
<td><p>%lastweek(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente à última semana.</p></td>
</tr>
<tr class="odd">
<td><p>nextmonth</p></td>
<td><p>%nextmonth(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade em um intervalo equivalente ao próximo mês.</p></td>
</tr>
<tr class="even">
<td><p>thismonth</p></td>
<td><p>%thismonth(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente a este mês.</p></td>
</tr>
<tr class="odd">
<td><p>lastmonth</p></td>
<td><p>%lastmonth(“SchemaName”)%</p></td>
<td><p>Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente ao último mês.</p></td>
</tr>
</tbody>
</table>


No exemplo a seguir DemoDASLDateMacro cria uma consulta DASL que usa a macro **lastmonthDateTime** para filtrar os itens na caixa de entrada do usuário que foram modificados no mês passado. Em seguida, cria um objeto **Table** com esse filtro, e enumera e exibe as linhas no objeto **Table** restrito.

Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

