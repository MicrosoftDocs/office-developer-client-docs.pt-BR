---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 447b7c609dd122d825d97a7430349eb88f8f7b0b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923949"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="1ea47-102">Propriedade DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1ea47-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="1ea47-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ea47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ea47-104">Indica a data da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="1ea47-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="1ea47-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1ea47-105">Return values</span></span>

<span data-ttu-id="1ea47-p101">Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="1ea47-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ea47-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ea47-108">Remarks</span></span>

<span data-ttu-id="1ea47-p102">A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="1ea47-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

