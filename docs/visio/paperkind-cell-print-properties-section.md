---
title: Célula PaperKind (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Especifica o tipo de papel no qual a página será impressa.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327059"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="46a08-103">Célula PaperKind (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="46a08-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="46a08-104">Especifica o tipo de papel no qual a página será impressa.</span><span class="sxs-lookup"><span data-stu-id="46a08-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46a08-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="46a08-105">Remarks</span></span>

<span data-ttu-id="46a08-106">Essa configuração corresponde à configuração **tamanho do papel** da caixa de diálogo **Configurar impressão** (na guia **design** , clique na seta **Configurar página** e, na guia **Configurar impressão** , clique no botão **Configurar** ).</span><span class="sxs-lookup"><span data-stu-id="46a08-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="46a08-107">Os valores numéricos nesta célula são mapeados como constantes (prefixadas com DMPAPER) definidas para seleções de papel no arquivo WinGDI. h do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="46a08-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="46a08-108">Para obter uma referência para a célula PaperKind pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="46a08-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46a08-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="46a08-109">Cell name:</span></span>  <br/> |<span data-ttu-id="46a08-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="46a08-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="46a08-111">Para obter uma referência para a célula PaperKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="46a08-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46a08-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="46a08-112">Section index:</span></span>  <br/> |<span data-ttu-id="46a08-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="46a08-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="46a08-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="46a08-114">Row index:</span></span>  <br/> |<span data-ttu-id="46a08-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="46a08-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="46a08-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="46a08-116">Cell index:</span></span>  <br/> |<span data-ttu-id="46a08-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="46a08-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

