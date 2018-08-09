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
description: Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771429"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="a4957-103">Célula ButtonFace (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="a4957-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="a4957-104">Identifica o ícone exibido ao lado de um item em um menu de atalho ou de ação de marca.</span><span class="sxs-lookup"><span data-stu-id="a4957-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a4957-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="a4957-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a4957-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4957-106">Remarks</span></span>

<span data-ttu-id="a4957-p101">A sequência de caracteres contida na célula ButtonFace representa a ID de uma imagem de face do botão do Microsoft Office. Um valor zero (0) ou em branco significa que nenhum ícone é exibido.</span><span class="sxs-lookup"><span data-stu-id="a4957-p101">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image. A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="a4957-109">As IDs que podem ser usadas na célula ButtonFace são os mesmos as IDs usadas com a propriedade **FaceID** de um objeto **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="a4957-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="a4957-110">Para obter mais detalhes sobre essas IDs, procure "Trabalhando com imagens de botão de barra de comandos" no MSDN.</span><span class="sxs-lookup"><span data-stu-id="a4957-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="a4957-111">Para obter uma referência para a célula ButtonFace pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a4957-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4957-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a4957-112">Cell name:</span></span>  <br/> |<span data-ttu-id="a4957-113">**Ações**.</span><span class="sxs-lookup"><span data-stu-id="a4957-113">**Actions**.</span></span>  <span data-ttu-id="a4957-114">*nome* .</span><span class="sxs-lookup"><span data-stu-id="a4957-114">*name*  .</span></span> <span data-ttu-id="a4957-115">**ButtonFace** onde **ações**.</span><span class="sxs-lookup"><span data-stu-id="a4957-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="a4957-116">*nome* é o nome da linha actions</span><span class="sxs-lookup"><span data-stu-id="a4957-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="a4957-117">Para fazer referência à célula ButtonFace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a4957-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4957-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a4957-118">Section index:</span></span>  <br/> |<span data-ttu-id="a4957-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a4957-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a4957-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a4957-120">Row index:</span></span>  <br/> |<span data-ttu-id="a4957-121">**visRowAction** +  *i* onde **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a4957-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a4957-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a4957-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a4957-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="a4957-123">**visActionButtonFace**</span></span> <br/> |
   

