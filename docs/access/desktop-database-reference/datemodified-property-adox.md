---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462297"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="dc9e4-102">Propriedade DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="dc9e4-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="dc9e4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc9e4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc9e4-104">Indica a data da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="dc9e4-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc9e4-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="dc9e4-105">Return Values</span></span>

<span data-ttu-id="dc9e4-p101">Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="dc9e4-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc9e4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc9e4-108">Remarks</span></span>

<span data-ttu-id="dc9e4-p102">A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="dc9e4-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

