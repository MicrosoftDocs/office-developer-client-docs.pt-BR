---
title: Procurar uma frase no corpo dos itens em uma pasta
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
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a><span data-ttu-id="bfcd3-102">Procurar uma frase no corpo dos itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="bfcd3-102">Search for a phrase in the body of items in a folder</span></span>

<span data-ttu-id="bfcd3-103">Este exemplo procura a cadeia de caracteres "office" no Corpo dos itens na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-103">This example searches for the string "office" in the Body of items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="bfcd3-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bfcd3-104">Example</span></span>

<span data-ttu-id="bfcd3-105">Este exemplo de código usa uma sintaxe DAV Searching and Locating (DASL) para especificar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="bfcd3-106">Para criar o filtro, o exemplo de código primeiro verifica se a Pesquisa Instantânea está habilitada no repositório padrão para determinar se a palavra-chave **ci\_phrasematch** será usada para haver uma correspondência exata de frase para "escritório" no corpo do item ou a palavra-chave **like** para corresponder a qualquer ocorrência de "office" como uma cadeia de caracteres exata ou uma subcadeia no corpo do item.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-106">To construct the filter, the code sample first checks if Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match of "office" in the item body, or the **like** keyword to match any occurrence of "office" as an exact string or a substring in the item body.</span></span> <span data-ttu-id="bfcd3-107">O exemplo aplica o filtro ao método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) na Caixa de Entrada e obtém os resultados em um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="bfcd3-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="bfcd3-108">O exemplo de código exibe o assunto de cada um dos itens retornados em **Table**.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="bfcd3-109">O exemplo de código especifica a propriedade **Body** usando a representação do namespace urn:schemas:httpmail:textdescription.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-109">The code sample specifies the **Body** property by using the namespace representation urn:schemas:httpmail:textdescription.</span></span>

<span data-ttu-id="bfcd3-110">A sintaxe para usar a palavra-chave **ci\_phrasematch** é:</span><span class="sxs-lookup"><span data-stu-id="bfcd3-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="bfcd3-111">A sintaxe para usar a palavra-chave **like** para correspondência de prefixo é:</span><span class="sxs-lookup"><span data-stu-id="bfcd3-111">The syntax for using the **like** keyword for prefix matching is:</span></span>

`<PropertySchemaName> like <Token>%`

<span data-ttu-id="bfcd3-112">A sintaxe para usar a palavra-chave **like** para qualquer correspondência de subcadeia de caracteres é:</span><span class="sxs-lookup"><span data-stu-id="bfcd3-112">The syntax for using the **like** keyword for any substring matching is:</span></span>

`<PropertySchemaName> like %<Token>%`

<span data-ttu-id="bfcd3-113">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bfcd3-114">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bfcd3-115">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="bfcd3-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="bfcd3-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfcd3-116">See also</span></span>

- [<span data-ttu-id="bfcd3-117">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="bfcd3-117">Search and filter</span></span>](search-and-filter.md)

