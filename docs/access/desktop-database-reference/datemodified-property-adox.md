---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726075"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="dc3c6-102">Propriedade DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="dc3c6-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="dc3c6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc3c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc3c6-104">Indica a data da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc3c6-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="dc3c6-105">Return values</span></span>

<span data-ttu-id="dc3c6-p101">Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc3c6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc3c6-108">Remarks</span></span>

<span data-ttu-id="dc3c6-p102">A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

