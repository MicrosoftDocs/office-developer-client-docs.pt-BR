---
title: Usar buscas instantâneas para pesquisar uma frase do assunto em todas as pastas e todas as lojas.
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709436"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>Usar buscas instantâneas para pesquisar uma frase do assunto em todas as pastas e todas as lojas.

Este exemplo usa a pesquisa instantânea para pesquisar uma frase do assunto em todas as pastas e todos os armazenamentos e exibir os itens em uma janela de navegador.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo a seguir é um trecho da [programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

A pesquisa instantânea é um recurso do Microsoft Outlook que permite pesquisar, emitindo consultas que retornam os resultados com base no conteúdo. Depois que sua consulta foi processada, os resultados podem ser retornados em uma variedade de objetos, incluindo o objeto[tabela](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), o conjunto de [itens](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) e o objeto [pesquisa](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) objeto. Você pode escrever o código que usa a pesquisa instantânea com a Sintaxe de Consulta Avançada (AQS) oferecida pela Microsoft Windows Desktop Search. AQS é um dos três idiomas de consulta que o Outlook dá suporte. É poderosa, mas é limitada à [pesquisa (cadeia de caracteres, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) método do objeto[Explorador](https://msdn.microsoft.com/library/bb623678\(v=office.15\)). É possível usar a AQS para fornecer uma restrição para **tabela** ou para os objetos do **Item**. Além disso, os resultados retornados por uma consulta AQS podem ser exibidos apenas na interface de usuário do Outlook. A tabela a seguir lista os três idiomas de consulta suportados pelo Outlook; No entanto, este tópico irá ilustrar somente o uso de AQS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Linguagem de consulta</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>A AQS é usada pelo Windows Desktop Search e é a linguagem de consulta para o recurso de pesquisa instantânea do Outlook.</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>A linguagem de pesquisa DAV para consulta e localização (DASL) se baseia na implementação do Microsoft Exchange DASL no Outlook. A DASL pode ser usada para retornar resultados no objeto <b>tabela</b>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>A linguagem de consulta Jet fornece uma linguagem de consulta simples para Outlook e com base no serviço Microsoft Jet Expression. Jet é usado para criar cadeias de caracteres de filtro para os métodos <b>restringir</b>, coleção de<b>itens</b>e o objeto <b>tabela</b>.</p></td>
</tr>
</tbody>
</table>


No exemplo de código a seguir, o DemoInstantSearch obtém todas as pastas de email de todas as lojas onde a indexação é habilitada usando a propriedade [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) do objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)). Ele usa o método **pesquisa** do objeto **Explorer** para filtrar por todos os itens que contêm a frase exata "Office 2007" no assunto e que foram recebidas no mês passado. Por fim, os resultados da pesquisa são exibidos em uma janela separada do Explorer.

Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. A declaração**usando** não deve se situar antes de funções no exemplo código mas devem ser adicionada antes da declaração classe pública. A seguinte linha de código mostra como fazer a importação e de tarefa em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)

