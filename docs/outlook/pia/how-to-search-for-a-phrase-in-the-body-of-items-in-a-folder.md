---
title: Pesquisar uma frase no corpo dos itens em uma pasta
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc8e0fb2b82ae9660e292a6ec1dea70e82fe36ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316027"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>Procurar uma frase no corpo dos itens em uma pasta

Este exemplo procura a cadeia de caracteres "office" no Corpo dos itens na Caixa de Entrada.

## <a name="example"></a>Exemplo

Este exemplo de código usa uma sintaxe DAV Searching and Locating (DASL) para especificar uma consulta. Para criar o filtro, o exemplo de código primeiro verifica se a Pesquisa Instantânea está habilitada no repositório padrão para determinar se a palavra-chave **ci\_phrasematch** será usada para haver uma correspondência exata de frase para "escritório" no corpo do item ou a palavra-chave **like** para corresponder a qualquer ocorrência de "office" como uma cadeia de caracteres exata ou uma subcadeia no corpo do item. O exemplo aplica o filtro ao método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) na Caixa de Entrada e obtém os resultados em um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)). O exemplo de código exibe o assunto de cada um dos itens retornados em **Table**.

O exemplo de código especifica a propriedade **Body** usando a representação do namespace urn:schemas:httpmail:textdescription.

A sintaxe para usar a palavra-chave **ci\_phrasematch** é:

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

A sintaxe para usar a palavra-chave **like** para correspondência de prefixo é:

`<PropertySchemaName> like <Token>%`

A sintaxe para usar a palavra-chave **like** para qualquer correspondência de subcadeia de caracteres é:

`<PropertySchemaName> like %<Token>%`

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
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

