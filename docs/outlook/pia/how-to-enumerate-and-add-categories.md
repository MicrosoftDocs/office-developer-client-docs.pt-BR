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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320409"
---
# <a name="enumerate-and-add-categories"></a><span data-ttu-id="f0e06-102">Enumerar e adicionar categorias</span><span class="sxs-lookup"><span data-stu-id="f0e06-102">Enumerate and add categories</span></span>

<span data-ttu-id="f0e06-103">Este exemplo mostra como enumerar categorias e adicionar uma categoria na lista categoria principal.</span><span class="sxs-lookup"><span data-stu-id="f0e06-103">This example shows how to enumerate categories and add a category to the main category list.</span></span>

## <a name="example"></a><span data-ttu-id="f0e06-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f0e06-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f0e06-105">O exemplo de código a seguir é um trecho da [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f0e06-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="f0e06-106">O modelo de objeto do Outlook oferece suporte à categorias que ajudam a organizar itens na caixa de entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0e06-106">The Outlook object model supports categories that help organize items in a user’s Inbox.</span></span> <span data-ttu-id="f0e06-107">Para manter o nível mais alto da organização, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f0e06-107">To maintain a higher level of organization, you can do the following:</span></span>

- <span data-ttu-id="f0e06-108">Categorize itens do Outlook e exiba-os por categoria.</span><span class="sxs-lookup"><span data-stu-id="f0e06-108">Categorize Outlook items and display them by category.</span></span>
- <span data-ttu-id="f0e06-109">Aplique várias categorias de cores a um único item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="f0e06-109">Apply multiple color categories to a single Outlook item.</span></span>
- <span data-ttu-id="f0e06-110">Agrupe e classifique os itens do Outlook por categoria de cores.</span><span class="sxs-lookup"><span data-stu-id="f0e06-110">Group and sort Outlook items by color category.</span></span>
- <span data-ttu-id="f0e06-111">Atribua teclas de atalho para cada categoria de cores, permitindo que os usuários possam categorizar itens mais facilmente.</span><span class="sxs-lookup"><span data-stu-id="f0e06-111">Assign shortcut keys to each color category, enabling users to more easily categorize items.</span></span>
- <span data-ttu-id="f0e06-112">Crie, exclua e altere as categorias de cores por programação ou por ação do usuário na interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="f0e06-112">Create, delete, and change color categories either programmatically, or by user action within the Outlook user interface.</span></span>

<span data-ttu-id="f0e06-113">Para expor o recurso de categorias, o modelo de objeto do Outlook fornece o objeto [categoria](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) que representa uma única categoria de cores definidas pelo usuário na lista categoria principal.</span><span class="sxs-lookup"><span data-stu-id="f0e06-113">To expose the functionality of categories, the Outlook object model provides a [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object that represents a single user-defined color category in the main category list.</span></span> <span data-ttu-id="f0e06-114">A lista Categoria principal contém categorias de cores que são apresentadas na interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="f0e06-114">The main category list contains color categories that are presented in the Outlook user interface.</span></span> <span data-ttu-id="f0e06-115">A lista é representada pelo conjunto [categorias](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) do objeto [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f0e06-115">The list is represented by the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="f0e06-116">Para criar um objeto **categoria**, use o método [adicionar (cadeia de caracteres, objeto, objeto)](https://msdn.microsoft.com/library/bb623093\(v=office.15\))do **conjunto** categorias.</span><span class="sxs-lookup"><span data-stu-id="f0e06-116">To create a **Category** object, use the [Add(String, Object, Object)](https://msdn.microsoft.com/library/bb623093\(v=office.15\)) method of the **Categories** collection.</span></span> <span data-ttu-id="f0e06-117">Quando você cria um objeto **categoria**um identificador global exclusivo (GUID) é criado, e esse identificador não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="f0e06-117">When you create a **Category** object, a globally unique identifier (GUID) is created, and this identifier cannot be changed.</span></span> <span data-ttu-id="f0e06-118">É representado pela propriedade[Idcategoria](https://msdn.microsoft.com/library/bb647100\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f0e06-118">It is represented by the [CategoryID](https://msdn.microsoft.com/library/bb647100\(v=office.15\)) property.</span></span> <span data-ttu-id="f0e06-119">No entanto, você pode alterar a chave de nome, a cor e o atalho associado a uma categoria de cores, definindo as propriedades[nome](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [cores](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), e [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)), respectivamente, da **categoria** em objeto.</span><span class="sxs-lookup"><span data-stu-id="f0e06-119">You can, however, change the name, color, and shortcut key associated with a color category by setting the [Name](https://msdn.microsoft.com/library/bb645577\(v=office.15\)), [Color](https://msdn.microsoft.com/library/bb612316\(v=office.15\)), and [ShortcutKey](https://msdn.microsoft.com/library/bb644944\(v=office.15\)) properties, respectively, of the **Category** object.</span></span> <span data-ttu-id="f0e06-120">Você pode alterar a propriedade **cor**definindo ou obtendo suas constantes [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f0e06-120">You can change the **Color** property by setting or getting its [OlCategoryColor](https://msdn.microsoft.com/library/bb608974\(v=office.15\)) constant.</span></span> <span data-ttu-id="f0e06-121">Para reproduzir a cor de um controle personalizado, use as seguintes propriedades de somente leitura do objeto**categoria**:</span><span class="sxs-lookup"><span data-stu-id="f0e06-121">To reproduce the color in a custom control, use the following read-only properties of the **Category** object:</span></span>

  - <span data-ttu-id="f0e06-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="f0e06-122">[CategoryBorderColor](https://msdn.microsoft.com/library/bb610083\(v=office.15\))</span></span>

  - <span data-ttu-id="f0e06-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="f0e06-123">[CategoryGradientBottomColor](https://msdn.microsoft.com/library/bb647357\(v=office.15\))</span></span>

  - <span data-ttu-id="f0e06-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span><span class="sxs-lookup"><span data-stu-id="f0e06-124">[CategoryGradientTopColor](https://msdn.microsoft.com/library/bb623975\(v=office.15\))</span></span>

<span data-ttu-id="f0e06-125">Essas propriedades retornam um valor**cor\_OLE** valor dependente da **propriedade** cor do **objeto** categoria.</span><span class="sxs-lookup"><span data-stu-id="f0e06-125">These properties return an **OLE\_COLOR** value, which is dependent on the **Color** property of the **Category** object.</span></span>

<span data-ttu-id="f0e06-126">Itens do Outlook são exibidos com base no nome da categoria.</span><span class="sxs-lookup"><span data-stu-id="f0e06-126">Outlook items are displayed based on the category name.</span></span> <span data-ttu-id="f0e06-127">Cada objeto do item tem a propriedade**categorias**que armazena uma cadeia de caracteres delimitada por vírgula e que representa os nomes das categorias.</span><span class="sxs-lookup"><span data-stu-id="f0e06-127">Each item object has a **Categories** property that stores a comma-delimited string that represents category names.</span></span> <span data-ttu-id="f0e06-128">(Por exemplo, para o objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , use a propriedade de \*\*\*\* [categorias](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) MailItem).</span><span class="sxs-lookup"><span data-stu-id="f0e06-128">(For example, for the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object, you would use the **MailItem** [Categories](https://msdn.microsoft.com/library/bb646442\(v=office.15\)) property).</span></span> <span data-ttu-id="f0e06-129">Isso permite que você adicione uma categoria para o item, mesmo se a categoria não estiver presente na lista de categorias.</span><span class="sxs-lookup"><span data-stu-id="f0e06-129">This enables you to add a category to the item, even if the category is not present in the main category list.</span></span>


> [!NOTE]
> <span data-ttu-id="f0e06-130">Se a propriedade **categorias** de um item contém um nome de categoria que não esteja na coleção**categorias** do objeto **NameSpace**, o nome da categoria associada ao item do Outlook será exibido, mas sem uma cor associada.</span><span class="sxs-lookup"><span data-stu-id="f0e06-130">If the **Categories** property of an item contains a category name that is not in the **Categories** collection of the **NameSpace** object, the category name associated with that Outlook item is displayed, but without an associated color.</span></span> <span data-ttu-id="f0e06-131">A propriedade **categorias**em um objeto **Item** não retorna a coleção **categorias**.</span><span class="sxs-lookup"><span data-stu-id="f0e06-131">The **Categories** property on an **Item** object does not return a **Categories** collection.</span></span>

<span data-ttu-id="f0e06-132">No exemplo código a seguir, o primeiro procedimento EnumerateCategories, é a lista principal do usuário de categorias representado pela coleção**categorias**.</span><span class="sxs-lookup"><span data-stu-id="f0e06-132">In the following code example, the first procedure, EnumerateCategories, gets the current user’s main list of categories, represented by the **Categories** collection.</span></span> <span data-ttu-id="f0e06-133">Em seguida enumera, o objeto**categoria**dessa coleção e escreve as propriedades**nome**e**Idcategoria** do  rastreamento de ouvintes na coleção[Ouvintes](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0e06-133">It then enumerates the **Category** objects in that collection, and writes the **Name** and **CategoryID** properties to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="f0e06-134">O segundo procedimento AddACategory, é a lista principal do usuário de categorias e usa o método CategoryExists para verificar se existe uma categoria chamada "ISV" no conjunto.</span><span class="sxs-lookup"><span data-stu-id="f0e06-134">The second procedure, AddACategory, gets the current user’s main list of categories and uses the CategoryExists method to check whether a category named “ISV” exists in the collection.</span></span> <span data-ttu-id="f0e06-135">Se nenhuma categoria com o nome "ISV" existir, o AddACategory adiciona uma categoria chamada "ISV" na lista de categoria principal e atribui uma cor escura azul usando a coleção**adicione** método da **categorias**.</span><span class="sxs-lookup"><span data-stu-id="f0e06-135">If no category with the name “ISV” exists, AddACategory adds a category named “ISV” to the main category list and assigns it a dark blue color by using the **Add** method of the **Categories** collection.</span></span> <span data-ttu-id="f0e06-136">Atribui CTRL + F11. como teclas de atalho para a categoria.</span><span class="sxs-lookup"><span data-stu-id="f0e06-136">It also assigns CTRL+F11 as the shortcut key for the category.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f0e06-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0e06-137">See also</span></span>

- [<span data-ttu-id="f0e06-138">Categorias de cor</span><span class="sxs-lookup"><span data-stu-id="f0e06-138">Color categories</span></span>](color-categories.md)

