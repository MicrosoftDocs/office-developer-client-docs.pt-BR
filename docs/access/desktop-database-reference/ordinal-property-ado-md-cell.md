---
title: Propriedade Ordinal (Cell do ADO MD)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa85626b0de3a907d5a7ebf79cf333f76f42426e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867976"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="87e43-102">Propriedade Ordinal (Cell do ADO MD)</span><span class="sxs-lookup"><span data-stu-id="87e43-102">Ordinal Property (ADO MD Cell)</span></span>


<span data-ttu-id="87e43-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="87e43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87e43-104">Identifica exclusivamente uma célula pela sua posição em um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="87e43-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="87e43-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="87e43-105">Return values</span></span>

<span data-ttu-id="87e43-106">Retorna um inteiro **Long** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="87e43-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="87e43-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="87e43-107">Remarks</span></span>

<span data-ttu-id="87e43-p101">O valor ordinal da célula identifica a célula de maneira exclusiva em um conjunto de células. Conceitualmente, células são numeradas em um conjunto de células como se o conjunto de células fosse uma matriz de *p* dimensões, em que *p* é o número de [eixos](axes-collection-ado-md.md). Células são numeradas começando do zero e ordenadas por linha.</span><span class="sxs-lookup"><span data-stu-id="87e43-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="87e43-111">O valor ordinal da célula pode ser usado com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md) para recuperar rapidamente a [Célula](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="87e43-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

