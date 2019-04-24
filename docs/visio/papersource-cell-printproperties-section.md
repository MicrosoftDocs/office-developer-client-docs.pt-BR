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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301460"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="273b5-103">Célula PaperSource (Seção PrintProperties)</span><span class="sxs-lookup"><span data-stu-id="273b5-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="273b5-104">Determina a fonte de papel para a página.</span><span class="sxs-lookup"><span data-stu-id="273b5-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="273b5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="273b5-105">Remarks</span></span>

<span data-ttu-id="273b5-106">Essa configuração corresponde à configuração **Fonte de Papel** da caixa de diálogo **Configurar Impressão** (na guia **Design**, clique na seta **Configurar Página** e, na guia **Configurar Impressão**, clique em **Configurar**).</span><span class="sxs-lookup"><span data-stu-id="273b5-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="273b5-107">Os valores numéricos nesta célula mapeiam as constantes (prefixadas com DMBIN) definidas para seleções de bin no arquivo WinGDI. h do Microsoft Windows; por exemplo, o valor 7 representa DMBIN_AUTO.</span><span class="sxs-lookup"><span data-stu-id="273b5-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="273b5-108">Para obter uma referência para a célula PaperSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="273b5-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="273b5-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="273b5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="273b5-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="273b5-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="273b5-111">Para obter uma referência para a célula PaperSource pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="273b5-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="273b5-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="273b5-112">Section index:</span></span>  <br/> |<span data-ttu-id="273b5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="273b5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="273b5-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="273b5-114">Row index:</span></span>  <br/> |<span data-ttu-id="273b5-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="273b5-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="273b5-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="273b5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="273b5-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="273b5-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

