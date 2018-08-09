---
title: Célula Name (Seção Reviewer)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: Contém o nome do revisor de um documento.
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772409"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="203a8-103">Célula Name (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="203a8-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="203a8-104">Contém o nome do revisor de um documento.</span><span class="sxs-lookup"><span data-stu-id="203a8-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="203a8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="203a8-105">Remarks</span></span>

 <span data-ttu-id="203a8-106">O valor padrão é o nome encontrado na caixa **nome** do usuário na guia **Geral** da caixa de diálogo **Opções do Visio** (clique na guia **arquivo** , clique em **Opções**e, em seguida, clique em **Geral**).</span><span class="sxs-lookup"><span data-stu-id="203a8-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="203a8-107">Para obter uma referência à célula Name pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="203a8-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="203a8-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="203a8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="203a8-109">Reviewer.Name [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="203a8-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="203a8-110">Para fazer referência à célula Name pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="203a8-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="203a8-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="203a8-111">Section index:</span></span>  <br/> |<span data-ttu-id="203a8-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="203a8-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="203a8-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="203a8-113">Row index:</span></span>  <br/> |<span data-ttu-id="203a8-114">**visRowReviewer** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="203a8-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="203a8-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="203a8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="203a8-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="203a8-116">**visReviewerName**</span></span> <br/> |
   

