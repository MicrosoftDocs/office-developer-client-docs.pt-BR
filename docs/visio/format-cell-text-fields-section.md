---
title: Célula Format (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm400
localization_priority: Normal
ms.assetid: ab937a00-84c2-6c1c-9080-b7c95ead4f63
description: Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou uma hora, uma duração ou uma moeda.
ms.openlocfilehash: c1c7fc7e9c699b7642369fbb979c005829b06cb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431516"
---
# <a name="format-cell-text-fields-section"></a><span data-ttu-id="d7a8c-103">Célula Format (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="d7a8c-103">Format Cell (Text Fields Section)</span></span>

<span data-ttu-id="d7a8c-104">Especifica a formatação de um campo de texto que pode ser uma sequência de caracteres, um número, uma data ou uma hora, uma duração ou uma moeda.</span><span class="sxs-lookup"><span data-stu-id="d7a8c-104">Specifies the formatting of a text field that is a string, a number, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7a8c-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7a8c-105">Remarks</span></span>

<span data-ttu-id="d7a8c-p101">Se o valor da célula Type for 0, 2, 5, 6 ou 7 (cadeia de caracteres, número, data ou hora, duração ou moeda, respectivamente), especifique uma figura de formatação apropriada para o tipo de dados. Por exemplo, a figura de formatação "# #/4 UU" formata o número 12,43 pol. como 12 2/4 POLEGADAS. Para obter mais informações sobre como especificar uma figura de formatação, consulte [Sobre figuras de formatação](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="d7a8c-p101">If the value of the Type cell is 0, 2, 5, 6, or 7 (string, number, date or time, duration, or currency, respectively), specify a format picture appropriate for the data type. For example, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="d7a8c-p102">Um número (Tipo = 2) pode representar uma dimensão, uma grandeza escalar, um ângulo, uma data, uma hora ou uma moeda. Para garantir que um número de entrada seja sempre avaliado como uma data, hora ou moeda, utilize as funções DATETIME ou CY na célula Format em vez de uma figura de formatação.</span><span class="sxs-lookup"><span data-stu-id="d7a8c-p102">A number (Type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="d7a8c-112">Para fazer referência à célula Format pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-112">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7a8c-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d7a8c-114">Fields.Format[  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d7a8c-114">Fields.Format[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d7a8c-115">Para fazer referência à célula Format pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-115">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7a8c-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-116">Section index:</span></span>  <br/> |<span data-ttu-id="d7a8c-117">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d7a8c-117">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d7a8c-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-118">Row index:</span></span>  <br/> |<span data-ttu-id="d7a8c-119">**visRowField**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7a8c-119">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7a8c-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d7a8c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d7a8c-121">**visFieldFormat**</span><span class="sxs-lookup"><span data-stu-id="d7a8c-121">**visFieldFormat**</span></span> <br/> |
   

