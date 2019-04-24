---
title: Célula Value (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contém o valor do item de dados de forma conforme inserido na caixa de diálogo Dados da Forma.
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355969"
---
# <a name="value-cell-shape-data-section"></a><span data-ttu-id="c9dac-103">Célula Value (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="c9dac-103">Value Cell (Shape Data Section)</span></span>

<span data-ttu-id="c9dac-104">Contém o valor do item de dados da forma inserido na caixa de diálogo **Definir Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="c9dac-104">Contains the shape data item's value as entered in the **Define Shape Data** dialog box.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c9dac-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9dac-105">Remarks</span></span>

<span data-ttu-id="c9dac-p101">As fórmulas inseridas nesta célula são substituídas por valores inseridos na caixa de diálogo **Definir Dados da Forma**. Isso acontecerá mesmo se você utilizar a função GUARD para proteger a fórmula.</span><span class="sxs-lookup"><span data-stu-id="c9dac-p101">Formulas entered in this cell are overridden by values entered in the **Define Shape Data** dialog box. This is true even if you use the GUARD function to protect the formula.</span></span> 
  
<span data-ttu-id="c9dac-108">Para obter uma referência para a célula Value pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c9dac-108">To get a reference to the Value cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9dac-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c9dac-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c9dac-110">Hélice.  *Nome* . Valor em que prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="c9dac-110">Prop.  *Name*  .Value where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c9dac-111">Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c9dac-111">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c9dac-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c9dac-112">Section index:</span></span>  <br/> |<span data-ttu-id="c9dac-113">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c9dac-113">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="c9dac-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c9dac-114">Row index:</span></span>  <br/> |<span data-ttu-id="c9dac-115">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c9dac-115">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c9dac-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c9dac-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c9dac-117">**visCustPropsValue**</span><span class="sxs-lookup"><span data-stu-id="c9dac-117">**visCustPropsValue**</span></span> <br/> |
   

