---
title: Célula Bullet (seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Determina o estilo de marcador.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422765"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="0095f-103">Célula Bullet (seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="0095f-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="0095f-104">Determina o estilo de marcador.</span><span class="sxs-lookup"><span data-stu-id="0095f-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="0095f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0095f-105">**Value**</span></span>|<span data-ttu-id="0095f-106">**Estilo de marcador**</span><span class="sxs-lookup"><span data-stu-id="0095f-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0095f-107">0</span><span class="sxs-lookup"><span data-stu-id="0095f-107">0</span></span>  <br/> |<span data-ttu-id="0095f-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0095f-108">None</span></span>  <br/> |
|<span data-ttu-id="0095f-109">1 </span><span class="sxs-lookup"><span data-stu-id="0095f-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="0095f-110">2 </span><span class="sxs-lookup"><span data-stu-id="0095f-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="0095f-111">3 </span><span class="sxs-lookup"><span data-stu-id="0095f-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="0095f-112">4 </span><span class="sxs-lookup"><span data-stu-id="0095f-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="0095f-113">5 </span><span class="sxs-lookup"><span data-stu-id="0095f-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="0095f-114">6 </span><span class="sxs-lookup"><span data-stu-id="0095f-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="0095f-115">7 </span><span class="sxs-lookup"><span data-stu-id="0095f-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="0095f-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0095f-116">Section index:</span></span>  <br/> |<span data-ttu-id="0095f-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="0095f-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="0095f-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="0095f-118">Row index:</span></span>  <br/> |<span data-ttu-id="0095f-119">**visRowParagraph**  +   *i* onde *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="0095f-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="0095f-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="0095f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0095f-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="0095f-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0095f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0095f-122">Remarks</span></span>

<span data-ttu-id="0095f-123">Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**.</span><span class="sxs-lookup"><span data-stu-id="0095f-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="0095f-124">Para obter uma referência para a célula Bullet pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="0095f-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0095f-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0095f-125">Cell name:</span></span>  <br/> |<span data-ttu-id="0095f-126">Para.Bullet[ *i*  ] onde  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="0095f-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="0095f-127">Para obter uma referência para a célula Bullet pelo índice, a partir de um programa, use a propriedade  **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0095f-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

