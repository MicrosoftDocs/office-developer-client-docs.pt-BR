---
title: Célula Initials (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: Contém as iniciais do revisor de um documento.
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772088"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="05790-103">Célula Initials (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="05790-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="05790-104">Contém as iniciais do revisor de um documento.</span><span class="sxs-lookup"><span data-stu-id="05790-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05790-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="05790-105">Remarks</span></span>

<span data-ttu-id="05790-106">Esse valor utiliza como padrão as iniciais na caixa **iniciais** , na guia **Geral** na caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , clique em **Opções**e, em seguida, clique em **Geral** ).</span><span class="sxs-lookup"><span data-stu-id="05790-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="05790-107">Para fazer referência à célula Initials pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="05790-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05790-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="05790-108">Cell name:</span></span>  <br/> | <span data-ttu-id="05790-109">Reviewer. Initials [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="05790-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="05790-110">Para fazer referência à célula Initials pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="05790-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05790-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="05790-111">Section index:</span></span>  <br/> |<span data-ttu-id="05790-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="05790-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="05790-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="05790-113">Row index:</span></span>  <br/> |<span data-ttu-id="05790-114">**visRowReviewer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="05790-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="05790-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="05790-115">Cell index:</span></span>  <br/> |<span data-ttu-id="05790-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="05790-116">**visReviewerInitials**</span></span> <br/> |
   

