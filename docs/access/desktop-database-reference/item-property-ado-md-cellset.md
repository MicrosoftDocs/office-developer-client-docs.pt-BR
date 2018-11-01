---
title: Propriedade Item (ADO MD Cellset)
TOCTitle: Item Property (ADO MD Cellset)
ms:assetid: 47510643-47af-0bfd-dc1f-ab984057bcd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249220(v=office.15)
ms:contentKeyID: 48544595
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d4f2f67daf4bf072037fac07ecdc3cd163904818
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883796"
---
# <a name="item-property-ado-md-cellset"></a><span data-ttu-id="d5562-102">Propriedade Item (ADO MD Cellset)</span><span class="sxs-lookup"><span data-stu-id="d5562-102">Item Property (ADO MD Cellset)</span></span>

<span data-ttu-id="d5562-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5562-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5562-104">Recupera uma célula de um conjunto de células usando suas coordenadas.</span><span class="sxs-lookup"><span data-stu-id="d5562-104">Retrieves a cell from a cellset using its coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5562-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5562-105">Syntax</span></span>

<span data-ttu-id="d5562-106">Definir*célula* = *Cellset*. Item (*posições*)</span><span class="sxs-lookup"><span data-stu-id="d5562-106">Set*Cell* = *Cellset*.Item (*Positions*)</span></span>

## <a name="parameters"></a><span data-ttu-id="d5562-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5562-107">Parameters</span></span>

- <span data-ttu-id="d5562-108">*Positions*</span><span class="sxs-lookup"><span data-stu-id="d5562-108">*Positions*</span></span>

- <span data-ttu-id="d5562-109">Um **Variant** **Array** de valores que especificam unicamente uma célula.</span><span class="sxs-lookup"><span data-stu-id="d5562-109">A **Variant** **Array** of values that uniquely specify a cell.</span></span> <span data-ttu-id="d5562-110">*Posições* pode ser um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="d5562-110">*Positions* can be one of the following:</span></span>
    
  - <span data-ttu-id="d5562-111">Uma matriz de números de posição</span><span class="sxs-lookup"><span data-stu-id="d5562-111">An array of position numbers</span></span>
    
  - <span data-ttu-id="d5562-112">Uma matriz de nomes de membros</span><span class="sxs-lookup"><span data-stu-id="d5562-112">An array of member names</span></span>
    
  - <span data-ttu-id="d5562-113">A posição ordinal</span><span class="sxs-lookup"><span data-stu-id="d5562-113">The ordinal position</span></span>

## <a name="remarks"></a><span data-ttu-id="d5562-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5562-114">Remarks</span></span>

<span data-ttu-id="d5562-115">Use a propriedade **Item** para retornar um objeto [Cell](cell-object-ado-md.md) em um objeto [Cellset](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d5562-115">Use the **Item** property to return a [Cell](cell-object-ado-md.md) object within a [Cellset](cellset-object-ado-md.md) object.</span></span> <span data-ttu-id="d5562-116">Se a propriedade **Item** não puder encontrar a célula correspondente ao argumento *posições* , ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="d5562-116">If the **Item** property cannot find the cell corresponding to the *Positions* argument, an error occurs.</span></span>

<span data-ttu-id="d5562-p103">A propriedade **Item** a propriedade padrão do objeto **Cellset**. As seguintes formas sintáticas são intercambiáveis:</span><span class="sxs-lookup"><span data-stu-id="d5562-p103">The **Item** property is the default property for the **Cellset** object. The following syntax forms are interchangeable:</span></span>

```vb
    Cellset.Item ( Positions )
    Cellset ( Positions )
```

<span data-ttu-id="d5562-119">O argumento *posições* Especifica qual célula para retornar.</span><span class="sxs-lookup"><span data-stu-id="d5562-119">The *Positions* argument specifies which cell to return.</span></span> <span data-ttu-id="d5562-120">Você pode especificar a célula por posição ordinal ou por posição ao longo de cada eixo.</span><span class="sxs-lookup"><span data-stu-id="d5562-120">You can specify the cell by ordinal position or by the position along each axis.</span></span> <span data-ttu-id="d5562-121">Ao especificar a célula por posição ao longo de cada eixo, você pode especificar o valor numérico da posição ou dos nomes dos membros de cada posição.</span><span class="sxs-lookup"><span data-stu-id="d5562-121">When specifying the cell by position along each axis, you can specify the numeric value of the position or the names of the members for each position.</span></span>

<span data-ttu-id="d5562-p105">A posição ordinal é um número que identifica uma célula de maneira exclusiva em um **Cellset**. Conceitualmente, células são numeradas em um **Cellset** como se o **Cellset** fosse uma matriz de *p* dimensões, em que *p* é o número de eixos. Células são endereçadas por ordem de linha.</span><span class="sxs-lookup"><span data-stu-id="d5562-p105">The ordinal position is a number that uniquely identifies one cell within the **Cellset**. Conceptually, cells are numbered in a **Cellset** as if the **Cellset** were a *p*-dimensional array, where *p* is the number of axes. Cells are addressed in row-major order.</span></span>

<span data-ttu-id="d5562-p106">Se nomes de membros são passados como cadeias de caracteres para **Item**, os membros devem ser listados em ordem crescente dos identificadores do eixo numérico. Em um eixo, os membros devem ser listados em ordem crescente de aninhamento de dimensão  ou seja, o membro da dimensão mais externa vem primeiro, seguido dos membros das dimensões internas. Cada dimensão deve ser representada por uma cadeia de caracteres separada, e a lista de cadeias de caracteres de membros deve ser separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="d5562-p106">If member names are passed as strings to **Item**, the members must be listed in increasing order of the numeric axis identifiers. Within an axis, the members must be listed in increasing order of dimension nesting — that is, the outermost dimension's member comes first, followed by members of inner dimensions. Each dimension should be represented by a separate string, and the list of member strings should be separated by commas.</span></span>


> [!NOTE]
> <span data-ttu-id="d5562-p107">[!OBSERVAçãO] Seu provedor de dados pode não oferecer suporte para recuperação de células por nome de membro. Consulte a documentação do seu provedor para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d5562-p107">Retrieving cells by member name may not be supported by your data provider. See the documentation for your provider for more information.</span></span>


