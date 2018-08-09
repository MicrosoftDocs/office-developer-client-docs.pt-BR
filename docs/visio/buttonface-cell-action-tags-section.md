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
description: Contém a identificação da imagem da face do botão exibido no botão de marca de ação.
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771430"
---
# <a name="buttonface-cell-action-tags-section"></a><span data-ttu-id="00b9c-103">Célula ButtonFace (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="00b9c-103">ButtonFace Cell (Action Tags Section)</span></span>

<span data-ttu-id="00b9c-104">Contém a identificação da imagem da face do botão exibido no botão de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="00b9c-104">Contains the ID of the button face image that appears on the action tag button.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00b9c-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="00b9c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00b9c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="00b9c-106">Remarks</span></span>

<span data-ttu-id="00b9c-107">A cadeia de caracteres contida na célula ButtonFace representa a identificação de uma imagem de face de botão do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="00b9c-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="00b9c-108">Um valor 0 (zero) ou deixe em branco, por padrão, o botão de informações de "i" de marca de ação padrão ![](media/InfoPS_ZA10180114.gif).</span><span class="sxs-lookup"><span data-stu-id="00b9c-108">A value of 0 (zero) or blank defaults to the standard action tag "i" info button ![](media/InfoPS_ZA10180114.gif).</span></span>
  
<span data-ttu-id="00b9c-109">As IDs que podem ser usadas na célula ButtonFace são os mesmos as IDs usadas com a propriedade **FaceID** de um objeto **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="00b9c-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="00b9c-110">Para obter mais detalhes sobre essas IDs, procure "Trabalhando com imagens de botão de barra de comandos" no MSDN.</span><span class="sxs-lookup"><span data-stu-id="00b9c-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="00b9c-111">Para fazer referência à célula ButtonFace pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="00b9c-111">To get a reference to the ButtonFace cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00b9c-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="00b9c-112">Cell name:</span></span>  <br/> | <span data-ttu-id="00b9c-113">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="00b9c-113">SmartTags.</span></span>  <span data-ttu-id="00b9c-114">*nome* . ButtonFace onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="00b9c-114">*name*  .ButtonFace           where SmartTags.</span></span> <span data-ttu-id="00b9c-115">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="00b9c-115">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="00b9c-116">Para fazer referência à célula ButtonFace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="00b9c-116">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00b9c-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="00b9c-117">Section index:</span></span>  <br/> |<span data-ttu-id="00b9c-118">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="00b9c-118">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="00b9c-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="00b9c-119">Row index:</span></span>  <br/> |<span data-ttu-id="00b9c-120">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="00b9c-120">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="00b9c-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="00b9c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="00b9c-122">**visSmartTagButtonFace**</span><span class="sxs-lookup"><span data-stu-id="00b9c-122">**visSmartTagButtonFace**</span></span> <br/> |
   

