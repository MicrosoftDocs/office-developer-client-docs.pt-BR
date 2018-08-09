---
title: Célula PaperSource (Seção PrintProperties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Determina a fonte de papel para a página.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772462"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="e52b8-103">Célula PaperSource (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="e52b8-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="e52b8-104">Determina a fonte de papel para a página.</span><span class="sxs-lookup"><span data-stu-id="e52b8-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e52b8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e52b8-105">Remarks</span></span>

<span data-ttu-id="e52b8-106">Essa configuração corresponde à configuração **Fonte de Papel** da caixa de diálogo **Configurar Impressão** (na guia **Design**, clique na seta **Configurar Página** e, na guia **Configurar Impressão**, clique em **Configurar**).</span><span class="sxs-lookup"><span data-stu-id="e52b8-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="e52b8-107">Os valores numéricos dessa célula são mapeados de acordo com constantes (prefixadas com DMBIN) definidos para seleções de compartimento no arquivo wingdi do Microsoft Windows; Por exemplo, o valor 7 representa DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="e52b8-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="e52b8-108">Para obter uma referência para a célula PaperSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e52b8-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e52b8-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e52b8-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e52b8-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="e52b8-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="e52b8-111">Para obter uma referência para a célula PaperSource pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e52b8-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e52b8-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e52b8-112">Section index:</span></span>  <br/> |<span data-ttu-id="e52b8-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e52b8-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e52b8-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e52b8-114">Row index:</span></span>  <br/> |<span data-ttu-id="e52b8-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e52b8-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e52b8-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e52b8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e52b8-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="e52b8-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

