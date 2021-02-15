---
title: Propriedade Ordinal (Cell do ADO MD)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 91b8d66929e360f88385b6773a03fcaffb79161d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288200"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="f617c-102">Propriedade Ordinal (Cell do ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f617c-102">Ordinal property (ADO MD Cell)</span></span>


<span data-ttu-id="f617c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f617c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f617c-104">Identifica exclusivamente uma célula pela sua posição em um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="f617c-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="f617c-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f617c-105">Return values</span></span>

<span data-ttu-id="f617c-106">Retorna um inteiro **Long** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f617c-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f617c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f617c-107">Remarks</span></span>

<span data-ttu-id="f617c-p101">O valor ordinal da célula identifica a célula de maneira exclusiva em um conjunto de células. Conceitualmente, células são numeradas em um conjunto de células como se o conjunto de células fosse uma matriz de *p* dimensões, em que *p* é o número de [eixos](axes-collection-ado-md.md). Células são numeradas começando do zero e ordenadas por linha.</span><span class="sxs-lookup"><span data-stu-id="f617c-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="f617c-111">O valor ordinal da célula pode ser usado com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md) para recuperar rapidamente a [Célula](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="f617c-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

