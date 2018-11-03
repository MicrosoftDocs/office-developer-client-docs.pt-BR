---
title: Propriedade Ordinal (Position do ADO MD)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abf355cc4d066604035fddbbe8f8a428d8c7a6b0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944778"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="15477-102">Propriedade Ordinal (Position do ADO MD)</span><span class="sxs-lookup"><span data-stu-id="15477-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="15477-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="15477-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15477-104">Identifica exclusivamente uma posição em um eixo.</span><span class="sxs-lookup"><span data-stu-id="15477-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="15477-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="15477-105">Return values</span></span>

<span data-ttu-id="15477-106">Retorna um inteiro **Long** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="15477-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="15477-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="15477-107">Remarks</span></span>

<span data-ttu-id="15477-108">O **Ordinal** de um objeto [Position](position-object-ado-md.md) corresponde ao índice do **Position** na coleção [Positions](positions-collection-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="15477-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="15477-109">Uma célula pode ser recuperada rapidamente por meio do **Ordinal** do objeto **Position** em cada eixo com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="15477-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

