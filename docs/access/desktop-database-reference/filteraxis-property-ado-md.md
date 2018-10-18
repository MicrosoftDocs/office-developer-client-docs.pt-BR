---
title: Propriedade FilterAxis (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603053"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="74acc-102">Propriedade FilterAxis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="74acc-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="74acc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74acc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="74acc-104">Indica informações de filtro sobre o conjunto de células atual.</span><span class="sxs-lookup"><span data-stu-id="74acc-104">Indicates filter information about the current cellset.</span></span>

<span data-ttu-id="74acc-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="74acc-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="74acc-106">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="74acc-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="74acc-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="74acc-107">Return values</span></span>
>>>>>>> <span data-ttu-id="74acc-108">mestre</span><span class="sxs-lookup"><span data-stu-id="74acc-108">master</span></span>

<span data-ttu-id="74acc-109">Retorna um objeto [Axis](axis-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="74acc-109">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="74acc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="74acc-110">Remarks</span></span>

<span data-ttu-id="74acc-p101">Use a propriedade **FilterAxis** para retornar informações sobre as dimensões que foram usadas para dividir os dados. A propriedade [DimensionCount](dimensioncount-property-ado-md.md) do **Axis** retorna o número de dimensões do slicer. Em geral, esse eixo tem apenas uma linha.</span><span class="sxs-lookup"><span data-stu-id="74acc-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="74acc-114">O **Axis** retornado pelo [FilterAxis](filteraxis-property-ado-md.md) não está contido na coleção [Axes](axes-collection-ado-md.md) de um objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="74acc-114">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

