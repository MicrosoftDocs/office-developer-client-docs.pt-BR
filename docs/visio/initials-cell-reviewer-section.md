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
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335291"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="4c302-103">Célula Initials (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="4c302-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="4c302-104">Contém as iniciais do revisor de um documento.</span><span class="sxs-lookup"><span data-stu-id="4c302-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c302-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c302-105">Remarks</span></span>

<span data-ttu-id="4c302-106">Este valor assume como padrão as iniciais na caixa **iniciais** da guia **geral** da caixa de diálogo opções do **Visio** (clique na guia **arquivo** , em **Opções**e em **geral** ).</span><span class="sxs-lookup"><span data-stu-id="4c302-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="4c302-107">Para fazer referência à célula Initials pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4c302-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c302-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4c302-108">Cell name:</span></span>  <br/> | <span data-ttu-id="4c302-109">Reviewer. Initials [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4c302-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4c302-110">Para fazer referência à célula Initials pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4c302-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4c302-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4c302-111">Section index:</span></span>  <br/> |<span data-ttu-id="4c302-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="4c302-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="4c302-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4c302-113">Row index:</span></span>  <br/> |<span data-ttu-id="4c302-114">**visRowReviewer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4c302-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4c302-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4c302-115">Cell index:</span></span>  <br/> |<span data-ttu-id="4c302-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="4c302-116">**visReviewerInitials**</span></span> <br/> |
   

