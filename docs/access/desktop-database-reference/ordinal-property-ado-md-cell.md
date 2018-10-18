---
title: Propriedade Ordinal (Cell do ADO MD)
TOCTitle: Ordinal Property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e067fbc90a0e05d31611d7284a735cf1cfe6aa1
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606777"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="7ea69-102">Propriedade Ordinal (Cell do ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7ea69-102">Ordinal Property (ADO MD Cell)</span></span>


<span data-ttu-id="7ea69-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ea69-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7ea69-104">Identifica exclusivamente uma célula pela sua posição em um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="7ea69-104">Uniquely identifies a cell by its position within a cellset.</span></span>

<span data-ttu-id="7ea69-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="7ea69-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="7ea69-106">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7ea69-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="7ea69-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7ea69-107">Return values</span></span>
>>>>>>> <span data-ttu-id="7ea69-108">mestre</span><span class="sxs-lookup"><span data-stu-id="7ea69-108">master</span></span>

<span data-ttu-id="7ea69-109">Retorna um inteiro **Long** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7ea69-109">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ea69-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ea69-110">Remarks</span></span>

<span data-ttu-id="7ea69-p101">O valor ordinal da célula identifica a célula de maneira exclusiva em um conjunto de células. Conceitualmente, células são numeradas em um conjunto de células como se o conjunto de células fosse uma matriz de *p* dimensões, em que *p* é o número de [eixos](axes-collection-ado-md.md). Células são numeradas começando do zero e ordenadas por linha.</span><span class="sxs-lookup"><span data-stu-id="7ea69-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="7ea69-114">O valor ordinal da célula pode ser usado com a propriedade [Item](item-property-ado-md-cellset.md) do objeto [Cellset](cellset-object-ado-md.md) para recuperar rapidamente a [Célula](cell-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="7ea69-114">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

