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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430942"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="8b00d-103">Célula Value (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="8b00d-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="8b00d-104">Contém a função para um campo.</span><span class="sxs-lookup"><span data-stu-id="8b00d-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b00d-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b00d-105">Remarks</span></span>

<span data-ttu-id="8b00d-106">Você pode definir o valor desta célula usando a caixa de diálogo **Campo** (na guia **Inserir**, do grupo **Texto**, clique em **Campo**).</span><span class="sxs-lookup"><span data-stu-id="8b00d-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="8b00d-107">Para fazer referência à célula Value pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8b00d-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b00d-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8b00d-108">Cell name:</span></span>  <br/> |<span data-ttu-id="8b00d-109">Fields. Value [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8b00d-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8b00d-110">Para fazer referência à célula Value pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8b00d-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b00d-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8b00d-111">Section index:</span></span>  <br/> |<span data-ttu-id="8b00d-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="8b00d-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="8b00d-113">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="8b00d-113">Row index:</span></span>  <br/> |<span data-ttu-id="8b00d-114">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8b00d-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="8b00d-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8b00d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8b00d-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="8b00d-116">**visFieldCell**</span></span> <br/> |
   

