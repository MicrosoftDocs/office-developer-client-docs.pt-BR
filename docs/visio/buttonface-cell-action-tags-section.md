---
title: Célula ButtonFace (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contém a ID da imagem de face do botão que é exibida no botão de marca de ação.
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337532"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="02c58-103">Célula ButtonFace (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="02c58-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="02c58-104">Contém a ID da imagem de face do botão que é exibida no botão de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="02c58-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="02c58-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="02c58-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02c58-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="02c58-106">Remarks</span></span>

<span data-ttu-id="02c58-p101">.A cadeia de caracteres contida na célula ButtonFace representa a identificação de uma imagem de face do botão do Microsoft Office. Um valor 0 (zero) ou em branco assume como padrão o botão de informação "i" da marca de ação</span><span class="sxs-lookup"><span data-stu-id="02c58-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of 0 (zero) or blank defaults to the standard action tag "i" info button</span></span> ![Botão de informação"i" da marca de ação padrão](media/InfoPS_ZA10180114.gif)<span data-ttu-id="02c58-110">.</span><span class="sxs-lookup"><span data-stu-id="02c58-110">.</span></span>
  
<span data-ttu-id="02c58-111">As identificações que podem ser usadas na célula ButtonFace são as mesmas que as utilizadas com a propriedade **FaceID** de um objeto **CommandBarButton**.</span><span class="sxs-lookup"><span data-stu-id="02c58-111">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="02c58-112">Para obter mais detalhes sobre essas identificações, procure "trabalhando com imagens de botão da barra de comandos" na MSDN.</span><span class="sxs-lookup"><span data-stu-id="02c58-112">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="02c58-113">Para obter uma referência à célula ButtonFace pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="02c58-113">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02c58-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="02c58-114">Cell name:</span></span>  <br/> | <span data-ttu-id="02c58-115">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="02c58-115">SmartTags.</span></span>  <span data-ttu-id="02c58-116">*name*  .ButtonFace           em que SmartTags.</span><span class="sxs-lookup"><span data-stu-id="02c58-116">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="02c58-117">*name*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="02c58-117">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="02c58-118">Para obter uma referência à célula ButtonFace pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="02c58-118">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02c58-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="02c58-119">Section index:</span></span>  <br/> |<span data-ttu-id="02c58-120">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="02c58-120">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="02c58-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="02c58-121">Row index:</span></span>  <br/> |<span data-ttu-id="02c58-122">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="02c58-122">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="02c58-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="02c58-123">Cell index:</span></span>  <br/> |<span data-ttu-id="02c58-124">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="02c58-124">**visSmartTagButtonFace**</span></span> <br/> |
   

