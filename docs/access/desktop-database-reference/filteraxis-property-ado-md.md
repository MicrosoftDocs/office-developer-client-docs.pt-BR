---
title: Propriedade FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 214de72e71a51c6b6b65bc2636a28e5650035c0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926903"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="d92f3-102">Propriedade FilterAxis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d92f3-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="d92f3-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d92f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d92f3-104">Indica informações de filtro sobre o conjunto de células atual.</span><span class="sxs-lookup"><span data-stu-id="d92f3-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="d92f3-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d92f3-105">Return values</span></span>

<span data-ttu-id="d92f3-106">Retorna um objeto [Axis](axis-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d92f3-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92f3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d92f3-107">Remarks</span></span>

<span data-ttu-id="d92f3-p101">Use a propriedade **FilterAxis** para retornar informações sobre as dimensões que foram usadas para dividir os dados. A propriedade [DimensionCount](dimensioncount-property-ado-md.md) do **Axis** retorna o número de dimensões do slicer. Em geral, esse eixo tem apenas uma linha.</span><span class="sxs-lookup"><span data-stu-id="d92f3-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="d92f3-111">O **Axis** retornado pelo [FilterAxis](filteraxis-property-ado-md.md) não está contido na coleção [Axes](axes-collection-ado-md.md) de um objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d92f3-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

