---
title: Obter informações sobre repositórios em um perfil
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2044fc52370bdadd5c7f01debbd02c88dd881715
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717192"
---
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="96309-102">Obter informações sobre repositórios em um perfil</span><span class="sxs-lookup"><span data-stu-id="96309-102">Get information about stores in a profile</span></span>

<span data-ttu-id="96309-103">Este exemplo mostra como acessar e enumerar repositórios em um perfil.</span><span class="sxs-lookup"><span data-stu-id="96309-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="96309-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="96309-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="96309-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="96309-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="96309-106">Você pode usar o conjunto [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) para enumerar os repositórios de um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="96309-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="96309-107">O conjunto **Stores** disponibiliza membros que expõem informações sobre cada objeto [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)), como quando um objeto **Store** é adicionado ou quando um objeto **Store** está prestes a ser removido no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="96309-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="96309-108">No exemplo de código a seguir, EnumerateStores recebe o objeto **Stores** que representa repositórios no perfil atual e enumera esses repositórios.</span><span class="sxs-lookup"><span data-stu-id="96309-108">In the following code example, EnumerateStores gets the **Stores** object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="96309-109">EnumerateStores examina cada objeto **Store** no conjunto **Stores**.</span><span class="sxs-lookup"><span data-stu-id="96309-109">EnumerateStores examines each **Store** object in the **Stores** collection.</span></span> <span data-ttu-id="96309-110">Se a propriedade [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) retornar **true**, indicando que é um repositório .pst ou .ost, as propriedades [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) e [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) serão gravadas para os ouvintes de rastreamento no conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="96309-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="96309-111">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="96309-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="96309-112">A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="96309-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="96309-113">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="96309-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="96309-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="96309-114">See also</span></span>

- [<span data-ttu-id="96309-115">Repositórios</span><span class="sxs-lookup"><span data-stu-id="96309-115">Stores</span></span>](stores.md)

