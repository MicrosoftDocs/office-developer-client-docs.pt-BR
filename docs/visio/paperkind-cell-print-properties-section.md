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
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772466"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="b28d4-103">Célula PaperKind (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="b28d4-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="b28d4-104">Especifica o tipo de papel no qual a página será impressa.</span><span class="sxs-lookup"><span data-stu-id="b28d4-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b28d4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b28d4-105">Remarks</span></span>

<span data-ttu-id="b28d4-106">Essa configuração corresponde à configuração de **Tamanho do papel** na caixa de diálogo **Configurar impressão** (na guia **Design** , clique na seta **Configurar página** e, em seguida, na guia **Configurar impressão** , clique no botão **Configurar** ).</span><span class="sxs-lookup"><span data-stu-id="b28d4-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="b28d4-107">Os valores numéricos dessa célula são mapeados de acordo com constantes (prefixadas com DMPAPER) definidas para seleções de papel no arquivo wingdi Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b28d4-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="b28d4-108">Para obter uma referência para a célula PaperKind pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b28d4-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b28d4-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b28d4-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b28d4-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="b28d4-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="b28d4-111">Para obter uma referência para a célula PaperKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b28d4-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b28d4-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b28d4-112">Section index:</span></span>  <br/> |<span data-ttu-id="b28d4-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b28d4-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b28d4-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b28d4-114">Row index:</span></span>  <br/> |<span data-ttu-id="b28d4-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b28d4-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b28d4-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b28d4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b28d4-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="b28d4-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

