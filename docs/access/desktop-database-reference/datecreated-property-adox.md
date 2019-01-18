---
title: Propriedade DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712614"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="bbf00-102">Propriedade DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="bbf00-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="bbf00-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbf00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbf00-104">Indica a data de criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="bbf00-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbf00-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="bbf00-105">Return values</span></span>

<span data-ttu-id="bbf00-p101">Retorna um valor **Variant** que especifica a data de criação. O valor será nulo se o provedor não oferecer suporte a **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="bbf00-p101">Returns a **Variant** value specifying the date created. The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf00-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbf00-108">Remarks</span></span>

<span data-ttu-id="bbf00-p102">A propriedade **DateCreated** é nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="bbf00-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

