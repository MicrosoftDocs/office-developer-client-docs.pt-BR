---
title: Pesquisar por uma frase exata em anexos de itens em uma pasta
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a937a273e0735b2d14369ae8cb8127e827501160
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819284"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="0064d-102">Pesquisar por uma frase exata em anexos de itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="0064d-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="0064d-103">Este exemplo procura a cadeia de caracteres de pesquisa exata "office" nos anexos de itens na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="0064d-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="0064d-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0064d-104">Example</span></span>

<span data-ttu-id="0064d-105">Este exemplo de código usa uma sintaxe DAV Searching and Locating (DASL) para especificar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="0064d-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="0064d-106">Para criar o filtro, o exemplo de código primeiro verifica se a Pesquisa Instantânea está habilitada no repositório padrão para determinar se a palavra-chave **ci\_phrasematch** será usada para haver uma correspondência exata de frase para "escritório" em qualquer anexo.</span><span class="sxs-lookup"><span data-stu-id="0064d-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="0064d-107">O exemplo aplica o filtro ao método [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) na Caixa de Entrada e obtém os resultados em um objeto [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="0064d-107">The sample then applies the filter to the [GetTable](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_MAPIFolder_GetTable_System_Object_System_Object_) method on the Inbox and obtains the results in a [Table](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.table?redirectedfrom=MSDN&view=outlook-pia) object.</span></span> <span data-ttu-id="0064d-108">O exemplo de código exibe o assunto de cada um dos itens retornados em **Table**.</span><span class="sxs-lookup"><span data-stu-id="0064d-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="0064d-109">O exemplo de código especifica a propriedade **Attachments** de um item usando a representação de namespace http://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span><span class="sxs-lookup"><span data-stu-id="0064d-109">The code sample specifies the **Attachments** property of an item using the namespace representation, http://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="0064d-110">A sintaxe para usar a palavra-chave **ci\_phrasematch** é:</span><span class="sxs-lookup"><span data-stu-id="0064d-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="0064d-111">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0064d-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0064d-112">A instrução **Imports** ou **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="0064d-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0064d-113">As linhas de código seguintes mostram como fazer a importação e a tarefa no Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="0064d-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```


```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0064d-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="0064d-114">See also</span></span>

- [<span data-ttu-id="0064d-115">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="0064d-115">Search and filter</span></span>](search-and-filter.md)

