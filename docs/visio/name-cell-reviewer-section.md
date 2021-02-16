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
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417683"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="b7b57-103">Célula Name (Seção Reviewer)</span><span class="sxs-lookup"><span data-stu-id="b7b57-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="b7b57-104">Contém o nome do revisor de um documento.</span><span class="sxs-lookup"><span data-stu-id="b7b57-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7b57-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7b57-105">Remarks</span></span>

 <span data-ttu-id="b7b57-106">Esse valor assume como padrão  o nome encontrado  na caixa Nome de usuário, na  guia Geral da caixa de diálogo Opções do **Visio** (clique na guia Arquivo, em Opções e em **Geral).**</span><span class="sxs-lookup"><span data-stu-id="b7b57-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="b7b57-107">Para fazer referência à célula Name pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="b7b57-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7b57-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b7b57-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b7b57-109">Reviewer.Name [  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b7b57-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b7b57-110">Para fazer referência à célula Name pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b7b57-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7b57-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b7b57-111">Section index:</span></span>  <br/> |<span data-ttu-id="b7b57-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="b7b57-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="b7b57-113">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b7b57-113">Row index:</span></span>  <br/> |<span data-ttu-id="b7b57-114">**visRowReviewer**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b7b57-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b7b57-115">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="b7b57-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b7b57-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="b7b57-116">**visReviewerName**</span></span> <br/> |
   

