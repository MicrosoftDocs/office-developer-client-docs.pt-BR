---
title: Célula ScaleX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Especifica o percentual de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772843"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="6bfbe-103">Célula ScaleX (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="6bfbe-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="6bfbe-104">Especifica o percentual de ampliação da página de desenho na página impressa.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bfbe-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bfbe-105">Remarks</span></span>

<span data-ttu-id="6bfbe-106">Esse valor é usado somente quando o valor da célula OnPage for FALSE.</span><span class="sxs-lookup"><span data-stu-id="6bfbe-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="6bfbe-107">As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor na configuração **Ajustar** da guia **Configurar impressão** , na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="6bfbe-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="6bfbe-108">Para obter uma referência para a célula ScaleX pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bfbe-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-109">Cell name:</span></span>  <br/> |<span data-ttu-id="6bfbe-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="6bfbe-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="6bfbe-111">Para obter uma referência para a célula ScaleX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bfbe-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-112">Section index:</span></span>  <br/> |<span data-ttu-id="6bfbe-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6bfbe-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6bfbe-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-114">Row index:</span></span>  <br/> |<span data-ttu-id="6bfbe-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="6bfbe-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="6bfbe-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6bfbe-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6bfbe-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="6bfbe-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

