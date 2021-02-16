---
title: Filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1c1702ce816714b21da860aea3e49db8a3511701
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542636"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a>Filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta

Este exemplo mostra como filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de dados de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). O objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) representa linhas de dados em uma **Table** (tabela). O objeto [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) representa propriedades de **Table**. Você pode adicionar certas propriedades ao objeto **Table** usando o método [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) do objeto **Columns**. Você pode filtrar certas propriedades usando o método [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) do objeto **Table**. No entanto, algumas propriedades não podem ser adicionadas ao objeto **Table** usando **Columns.Add**, e também não podem ser filtrados com o uso do método **Restrict**. A tabela a seguir descreve se propriedades têm suporte para o objeto **Table** quando se usa o método **Columns.Add** ou **Restrict**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriedade</p></th>
<th><p>Para Columns.Add</p></th>
<th><p>Para Restrict</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Propriedades binárias como <b>EntryID</b>.</p></td>
<td><p>Suporte por meio de propriedade interna ou de namespace.</p></td>
<td><p>Sem suporte. O Outlook irá gerar um erro.</p></td>
</tr>
<tr class="even">
<td><p>Propriedades do corpo, incluindo <b>Body</b> e <b>HTMLBody</b>, e representação do namespace dessas propriedades, incluindo <b>PR_RTF_COMPRESSED</b>.</p></td>
<td><p>A propriedade <b>Body</b> é suportada com a condição de que somente os primeiros 255 bytes do valor sejam armazenados em um objeto <b>Table</b>. Não há suporte para outras propriedades que representam o conteúdo do corpo em HTML ou RTF. Pelo motivo de somente os primeiros 255 bytes de <b>Body</b> serem retornados, se você quiser obter o conteúdo completo do corpo de um item em texto ou HTML, use o <b>EntryID</b> do item no método <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> para obter o objeto do item. Depois, recupere o valor completo de <b>Body</b> através do objeto do item.</p></td>
<td><p>Somente a propriedade <b>Body</b> representada em texto tem suporte em um filtro. Isso significa que a propriedade deve ser referenciada em um filtro DAV Searching and Locating (DASL) como <em>urn:schemas:http-email:textdescription</em>, e você não pode filtrar nenhuma marca HTML no corpo. Para melhorar o desempenho, use palavras-chave do indexador de contexto no filtro para combinar cadeias de caracteres no corpo.</p></td>
</tr>
<tr class="odd">
<td><p>Propriedades do computador, como <b>AutoResolvedWinner</b> e <b>BodyFormat</b>.</p></td>
<td><p>Sem suporte.</p></td>
<td><p>Sem suporte.</p></td>
</tr>
<tr class="even">
<td><p>Propriedades de valores múltiplos, como <b>Categories</b>, <b>Children</b>, <b>Companies</b> e <b>VotingOptions</b>.</p></td>
<td><p>Com suporte.</p></td>
<td><p>Com suporte, desde que você possa criar uma consulta DASL usando a representação do namespace.</p></td>
</tr>
<tr class="odd">
<td><p>Propriedades que retornam um objeto, como <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> e <b>UserProperties</b>.</p></td>
<td><p>Sem suporte.</p></td>
<td><p>Sem suporte.</p></td>
</tr>
</tbody>
</table>


A tabela a seguir lista as propriedades inválidas conhecidas que não podem ser adicionadas ao objeto **Table** com o uso de **Columns.Add**. Se você tentar adicionar uma propriedade desta lista, o Outlook irá gerar um erro.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>AutoResolvedWinner</p></td>
<td><p>BodyFormat</p></td>
<td><p>Classe</p></td>
</tr>
<tr class="even">
<td><p>Empresas</p></td>
<td><p>ContactNames</p></td>
<td><p>DLName</p></td>
</tr>
<tr class="odd">
<td><p>DownloadState</p></td>
<td><p>FlagIcon</p></td>
<td><p>HtmlBody</p></td>
</tr>
<tr class="even">
<td><p>InternetCodePage</p></td>
<td><p>IsConflict</p></td>
<td><p>IsMarkedAsTask</p></td>
</tr>
<tr class="odd">
<td><p>MeetingWorkspaceURL</p></td>
<td><p>MemberCount</p></td>
<td><p>Permissão</p></td>
</tr>
<tr class="even">
<td><p>PermissionService</p></td>
<td><p>RecurrenceState</p></td>
<td><p>ResponseState</p></td>
</tr>
<tr class="odd">
<td><p>Saved</p></td>
<td><p>Sent</p></td>
<td><p>Submitted</p></td>
</tr>
<tr class="even">
<td><p>TaskSubject</p></td>
<td><p>Unread</p></td>
<td><p>VotingOptions</p></td>
</tr>
</tbody>
</table>


Embora algumas propriedades calculadas não possam ser adicionadas à coluna definida para uma tabela, o seguinte exemplo de código funciona para contornar esta limitação. GetToDoItems usa uma consulta DASL para restringir os itens que aparecem em **Table**. Se a propriedade computada tem uma representação de namespace, a representação de namespace é usada para criar uma consulta DASL que restringe o objeto **Table** para retornar linhas de um valor específico da propriedade calculada. GetToDoItems coloca itens na Caixa de Entrada onde o valor da propriedade [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) é igual a **verdadeiro**, e depois atribui valores a determinadas propriedades de tarefas como [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) e [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)). Finalmente, essas propriedades são escritas para rastrear ouvintes da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "http://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "http://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

