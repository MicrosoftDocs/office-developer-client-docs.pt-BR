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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294418"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="be2ad-102">Propriedade DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="be2ad-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="be2ad-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be2ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be2ad-104">Indica a data de criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="be2ad-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="be2ad-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="be2ad-105">Return values</span></span>

<span data-ttu-id="be2ad-106">Retorna um valor **Variant** que especifica a data de criação.</span><span class="sxs-lookup"><span data-stu-id="be2ad-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="be2ad-107">O valor será nulo se o provedor não oferecer suporte a **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="be2ad-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="be2ad-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="be2ad-108">Remarks</span></span>

<span data-ttu-id="be2ad-p102">A propriedade **DateCreated** é nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateCreated**.</span><span class="sxs-lookup"><span data-stu-id="be2ad-p102">The **DateCreated** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>

