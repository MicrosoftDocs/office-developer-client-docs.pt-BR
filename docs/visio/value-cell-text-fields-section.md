---
title: Célula Value (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Contém a função para um campo.
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320199"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="332d4-103">Célula Value (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="332d4-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="332d4-104">Contém a função para um campo.</span><span class="sxs-lookup"><span data-stu-id="332d4-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="332d4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="332d4-105">Remarks</span></span>

<span data-ttu-id="332d4-106">Você pode definir o valor desta célula usando a caixa de diálogo **Campo** (na guia **Inserir**, do grupo **Texto**, clique em **Campo**).</span><span class="sxs-lookup"><span data-stu-id="332d4-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="332d4-107">Para fazer referência à célula Value pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="332d4-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="332d4-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="332d4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="332d4-109">Fields. Value [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="332d4-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="332d4-110">Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="332d4-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="332d4-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="332d4-111">Section index:</span></span>  <br/> |<span data-ttu-id="332d4-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="332d4-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="332d4-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="332d4-113">Row index:</span></span>  <br/> |<span data-ttu-id="332d4-114">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="332d4-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="332d4-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="332d4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="332d4-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="332d4-116">**visFieldCell**</span></span> <br/> |
   

