---
title: Enumerar e adicionar categorias
TOCTitle: Enumerate and add categories
ms:assetid: 17a94a01-c463-4332-851e-7d280c66d8c2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424467(v=office.15)
ms:contentKeyID: 55119829
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e00971adb1f2fa38555039478ac830d3c9f7a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717752"
---
# <a name="enumerate-and-add-categories"></a>Enumerar e adicionar categorias

Este exemplo mostra como enumerar categorias e adicionar uma categoria na lista categoria principal.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O modelo de objeto do Outlook oferece suporte à categorias que ajudam a organizar itens na caixa de entrada do usuário. Para manter o nível mais alto da organização, faça o seguinte:

- Categorize itens do Outlook e exiba-os por categoria.
- Aplique várias categorias de cores a um único item do Outlook.
- Agrupe e classifique os itens do Outlook por categoria de cores.
- Atribua teclas de atalho para cada categoria de cores, permitindo que os usuários possam categorizar itens mais facilmente.
- Crie, exclua e altere as categorias de cores por programação ou por ação do usuário na interface de usuário do Outlook.

Para expor o recurso de categorias, o modelo de objeto do Outlook fornece o objeto [categoria](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) que representa uma única categoria de cores definidas pelo usuário na lista categoria principal. A lista Categoria principal contém categorias de cores que são apresentadas na interface de usuário do Outlook. A lista é representada pelo conjunto [categorias](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Para criar um objeto **categoria**, use o método [adicionar (cadeia de caracteres, objeto, objeto)](https://msdn.microsoft.com/library/bb623093\(v=office.15\))do **conjunto** categorias. Quando você cria um objeto **categoria**um identificador global exclusivo (GUID) é criado, e esse identificador não pode ser alterado. É representado pela propriedade[Idcategoria](https://msdn.microsoft.com/library/bb647100\(v=office.15\)). No entanto, você pode alterar a chave de nome, a cor e o atalho associado a uma categoria de cores, definindo as propriedades[nome](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [cores](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), e [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)), respectivamente, da **categoria** em objeto. Você pode alterar a propriedade **cor**definindo ou obtendo suas constantes [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)). Para reproduzir a cor de um controle personalizado, use as seguintes propriedades de somente leitura do objeto**categoria**:

  - [CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))

  - [CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))

  - [CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))

Essas propriedades retornam um valor**cor\_OLE** valor dependente da **propriedade** cor do **objeto** categoria.

Itens do Outlook são exibidos com base no nome da categoria. Cada objeto do item tem a propriedade**categorias**que armazena uma cadeia de caracteres delimitada por vírgula e que representa os nomes das categorias. (Por exemplo, para o objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , você usaria a propriedade [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) **MailItem**). Isso permite que você adicione uma categoria para o item, mesmo se a categoria não estiver presente na lista de categorias.


> [!NOTE]
> Se a propriedade **categorias** de um item contém um nome de categoria que não esteja na coleção**categorias** do objeto **NameSpace**, o nome da categoria associada ao item do Outlook será exibido, mas sem uma cor associada. A propriedade **categorias**em um objeto **Item** não retorna a coleção **categorias**.

No exemplo código a seguir, o primeiro procedimento EnumerateCategories, é a lista principal do usuário de categorias representado pela coleção**categorias**. Em seguida enumera, o objeto**categoria**dessa coleção e escreve as propriedades**nome**e**Idcategoria** do  rastreamento de ouvintes na coleção[Ouvintes](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx). O segundo procedimento AddACategory, é a lista principal do usuário de categorias e usa o método CategoryExists para verificar se existe uma categoria chamada "ISV" no conjunto. Se nenhuma categoria com o nome "ISV" existir, o AddACategory adiciona uma categoria chamada "ISV" na lista de categoria principal e atribui uma cor escura azul usando a coleção**adicione** método da **categorias**. Atribui CTRL + F11. como teclas de atalho para a categoria.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateCategories()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    foreach (Outlook.Category category in categories)
    {
        Debug.WriteLine(category.Name);
        Debug.WriteLine(category.CategoryID);
    }
}

private void AddACategory()
{
    Outlook.Categories categories =
        Application.Session.Categories;
    if (!CategoryExists("ISV"))
    {
        Outlook.Category category = categories.Add("ISV",
            Outlook.OlCategoryColor.olCategoryColorDarkBlue,
            Outlook.OlCategoryShortcutKey.olCategoryShortcutKeyCtrlF11);
    }
}

private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category = 
            Application.Session.Categories[categoryName];
        if(category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Confira também

- [Categorias de cor](color-categories.md)

