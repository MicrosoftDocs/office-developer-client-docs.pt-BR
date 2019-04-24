---
title: Propriedade FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292451"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="df5be-102">Propriedade FilterAxis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="df5be-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="df5be-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df5be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df5be-104">Indica informações de filtro sobre o conjunto de células atual.</span><span class="sxs-lookup"><span data-stu-id="df5be-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="df5be-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="df5be-105">Return values</span></span>

<span data-ttu-id="df5be-106">Retorna um objeto [Axis](axis-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="df5be-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="df5be-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="df5be-107">Remarks</span></span>

<span data-ttu-id="df5be-p101">Use a propriedade **FilterAxis** para retornar informações sobre as dimensões que foram usadas para dividir os dados. A propriedade [DimensionCount](dimensioncount-property-ado-md.md) do **Axis** retorna o número de dimensões do slicer. Em geral, esse eixo tem apenas uma linha.</span><span class="sxs-lookup"><span data-stu-id="df5be-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="df5be-111">O **Axis** retornado pelo [FilterAxis](filteraxis-property-ado-md.md) não está contido na coleção [Axes](axes-collection-ado-md.md) de um objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="df5be-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

