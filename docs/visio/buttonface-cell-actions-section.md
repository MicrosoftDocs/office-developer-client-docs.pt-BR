---
title: Célula ButtonFace (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifica o ícone exibido ao lado de um item em um menu de atalho ou de marca de ação.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337545"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="88d0e-103">Célula ButtonFace (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="88d0e-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="88d0e-104">Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.</span><span class="sxs-lookup"><span data-stu-id="88d0e-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="88d0e-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="88d0e-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="88d0e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="88d0e-106">Remarks</span></span>

<span data-ttu-id="88d0e-p101">A sequência de caracteres contida na célula ButtonFace representa a ID de uma imagem de face do botão do Microsoft Office. Um valor zero (0) ou em branco significa que nenhum ícone é exibido.</span><span class="sxs-lookup"><span data-stu-id="88d0e-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="88d0e-109">As identificações que podem ser usadas na célula ButtonFace são as mesmas que as utilizadas com a propriedade **FaceID** de um objeto **CommandBarButton**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="88d0e-110">Para obter mais detalhes sobre essas identificações, procure "trabalhando com imagens de botão da barra de comandos" na MSDN.</span><span class="sxs-lookup"><span data-stu-id="88d0e-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="88d0e-111">Para obter uma referência para a célula ButtonFace pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="88d0e-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88d0e-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="88d0e-112">Cell name:</span></span>  <br/> |<span data-ttu-id="88d0e-113">**Ações**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-113">**Actions**.</span></span>  <span data-ttu-id="88d0e-114">*nome* .</span><span class="sxs-lookup"><span data-stu-id="88d0e-114">*name*  .</span></span> <span data-ttu-id="88d0e-115">**ButtonFace** onde **Actions**.</span><span class="sxs-lookup"><span data-stu-id="88d0e-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="88d0e-116">*Name* é o nome da linha de ações</span><span class="sxs-lookup"><span data-stu-id="88d0e-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="88d0e-117">Para fazer referência à célula ButtonFace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="88d0e-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="88d0e-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="88d0e-118">Section index:</span></span>  <br/> |<span data-ttu-id="88d0e-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="88d0e-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="88d0e-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="88d0e-120">Row index:</span></span>  <br/> |<span data-ttu-id="88d0e-121">**visRowAction** +  *i* onde **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="88d0e-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="88d0e-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="88d0e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="88d0e-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="88d0e-123">**visActionButtonFace**</span></span> <br/> |
   

