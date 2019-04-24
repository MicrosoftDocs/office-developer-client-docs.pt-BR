---
title: Exibir itens selecionados no Explorer ativo
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b722bcb404f987a6f07a9fe305046ea6673dc231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356382"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="bcd8b-102">Exibir itens selecionados no Explorer ativo</span><span class="sxs-lookup"><span data-stu-id="bcd8b-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="bcd8b-103">Este exemplo mostra como usar a classe auxiliar OutlookItem para exibir convenientemente todos os itens escolhidos na janela ativa do Explorer.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="bcd8b-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bcd8b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bcd8b-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="bcd8b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="bcd8b-106">O objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) contém o conjunto de itens do Outlook atualmente escolhidos no explorador ativo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="bcd8b-107">Nem o explorador ativo, representado pelo [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nem o conjunto de itens escolhidos indica o tipo dos itens escolhidos.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)), nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="bcd8b-108">Normalmente, você teria que primeiro identificar o tipo de item e, em seguida, chamar o método **Display** específico para esse tipo.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="bcd8b-109">Como o método **Display** é comum para todos os objetos de itens do Outlook e a classe auxiliar OutlookItem inclui esse método, aproveite a classe auxiliar declarando uma instância do objeto OutlookItem, myItem e utilize myItem.Display para exibir cada item na seleção.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-109">Because the **Display** method is common to all Outlook items objects and the OutlookItem helper class includes this method, you can take advantage of the helper class, by declaring an instance of the OutlookItem object, myItem, and using myItem.Display to display each item in the selection.</span></span> <span data-ttu-id="bcd8b-110">Você pode ver a implementação da classe auxiliar OutlookItem em [Criar uma classe auxiliar para acessar membros de itens comuns do Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span><span class="sxs-lookup"><span data-stu-id="bcd8b-110">You can see the implementation of the OutlookItem helper class in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)</span></span>

<span data-ttu-id="bcd8b-111">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bcd8b-112">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bcd8b-113">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="bcd8b-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bcd8b-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcd8b-114">See also</span></span>

- [<span data-ttu-id="bcd8b-115">Criar uma classe auxiliar para acessar membros comuns do item do Outlook</span><span class="sxs-lookup"><span data-stu-id="bcd8b-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="bcd8b-116">Itens gerais do Outlook</span><span class="sxs-lookup"><span data-stu-id="bcd8b-116">General Outlook items</span></span>](general-outlook-items.md)

