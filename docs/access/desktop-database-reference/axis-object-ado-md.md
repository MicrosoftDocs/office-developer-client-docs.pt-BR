---
title: Objeto Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e90ff31c0b6a78a3f242927e2fa7e84c42d6ab3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945345"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="fddde-102">Objeto Axis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fddde-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="fddde-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="fddde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fddde-104">Representa um eixo de posição ou de filtro de um conjunto de células, contendo membros selecionados de uma ou mais dimensões.</span><span class="sxs-lookup"><span data-stu-id="fddde-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="fddde-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="fddde-105">Remarks</span></span>

<span data-ttu-id="fddde-106">Um objeto **Axis** pode estar contido em uma coleção [Axes](axes-collection-ado-md.md)ou retornado pela propriedade [FilterAxis](filteraxis-property-ado-md.md) de um [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fddde-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="fddde-107">Com as coleções e as propriedades de um objeto **Axis**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="fddde-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="fddde-108">Identificar o **Eixo** com a propriedade [Name](name-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fddde-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="fddde-109">Percorrer cada posição ao longo de um **Eixo** usando a coleção [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fddde-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="fddde-110">Obter o número de dimensões no **Eixo** com a propriedade [DimensionCount](dimensioncount-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="fddde-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="fddde-111">Obter atributos específicos do provedor do **Eixo** com a coleção [Properties](properties-collection-ado.md) padrão do ADO.</span><span class="sxs-lookup"><span data-stu-id="fddde-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

