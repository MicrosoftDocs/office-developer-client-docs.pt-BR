---
title: Propriedade DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 344b193b3ab8d6800fcf81b6bb2d184b1104f9d3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923095"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="b73ea-102">Propriedade DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b73ea-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="b73ea-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b73ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b73ea-104">Indica a data de criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="b73ea-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="b73ea-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b73ea-105">Return values</span></span>

<span data-ttu-id="b73ea-p101">Retorna um valor **Variant** que especifica a data de criação. O valor será nulo se o provedor não oferecer suporte a **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="b73ea-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="b73ea-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b73ea-108">Remarks</span></span>

<span data-ttu-id="b73ea-p102">A propriedade **DateCreated** é nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="b73ea-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

