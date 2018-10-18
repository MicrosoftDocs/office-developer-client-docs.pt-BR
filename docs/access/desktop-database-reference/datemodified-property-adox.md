---
title: Propriedade DateModified (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603326"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="9aac9-102">Propriedade DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9aac9-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="9aac9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aac9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9aac9-104">Indica a data da última modificação do objeto.</span><span class="sxs-lookup"><span data-stu-id="9aac9-104">Indicates the date the object was last modified.</span></span>

<span data-ttu-id="9aac9-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="9aac9-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="9aac9-106">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="9aac9-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="9aac9-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9aac9-107">Return values</span></span>
>>>>>>> <span data-ttu-id="9aac9-108">mestre</span><span class="sxs-lookup"><span data-stu-id="9aac9-108">master</span></span>

<span data-ttu-id="9aac9-p101">Retorna um valor **Variant** que especifica a data de modificação. O valor será nulo se o provedor não oferecer suporte a **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="9aac9-p101">Returns a **Variant** value specifying the date modified. The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aac9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aac9-111">Remarks</span></span>

<span data-ttu-id="9aac9-p102">A propriedade **DateModified** será nula para objetos recém-acrescentados. Após acrescentar um novo [Modo de exibição](view-object-adox.md) ou [Procedimento](procedure-object-adox.md), chame o método [Refresh](refresh-method-ado.md) da coleção [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) para obter valores da propriedade **DateModified**.</span><span class="sxs-lookup"><span data-stu-id="9aac9-p102">The **DateModified** property is null for newly appended objects. After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>

