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
description: Determina o estilo com marcadores.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771433"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="6dfd0-103">Célula Bullet (seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="6dfd0-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="6dfd0-104">Determina o estilo com marcadores.</span><span class="sxs-lookup"><span data-stu-id="6dfd0-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="6dfd0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6dfd0-105">**Value**</span></span>|<span data-ttu-id="6dfd0-106">**Estilo com marcadores**</span><span class="sxs-lookup"><span data-stu-id="6dfd0-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6dfd0-107">0</span><span class="sxs-lookup"><span data-stu-id="6dfd0-107">0</span></span>  <br/> |<span data-ttu-id="6dfd0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6dfd0-108">None</span></span>  <br/> |
|<span data-ttu-id="6dfd0-109">1</span><span class="sxs-lookup"><span data-stu-id="6dfd0-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="6dfd0-110">2</span><span class="sxs-lookup"><span data-stu-id="6dfd0-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="6dfd0-111">3</span><span class="sxs-lookup"><span data-stu-id="6dfd0-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="6dfd0-112">4</span><span class="sxs-lookup"><span data-stu-id="6dfd0-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="6dfd0-113">5</span><span class="sxs-lookup"><span data-stu-id="6dfd0-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="6dfd0-114">6</span><span class="sxs-lookup"><span data-stu-id="6dfd0-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="6dfd0-115">7</span><span class="sxs-lookup"><span data-stu-id="6dfd0-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="6dfd0-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-116">Section index:</span></span>  <br/> |<span data-ttu-id="6dfd0-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="6dfd0-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="6dfd0-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-118">Row index:</span></span>  <br/> |<span data-ttu-id="6dfd0-119">**visRowParagraph** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="6dfd0-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="6dfd0-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6dfd0-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="6dfd0-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6dfd0-122">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6dfd0-122">Remarks</span></span>

<span data-ttu-id="6dfd0-123">Você pode também definir o valor desta célula clicando duas vezes uma forma, apontando para **Formatar**, clicando em **texto**e, em seguida, clicando na guia **marcadores** .</span><span class="sxs-lookup"><span data-stu-id="6dfd0-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="6dfd0-124">Para obter uma referência para a célula Bullet pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6dfd0-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-125">Cell name:</span></span>  <br/> |<span data-ttu-id="6dfd0-126">Para.Bullet [ *i* ] onde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="6dfd0-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="6dfd0-127">Para obter uma referência para a célula Bullet pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6dfd0-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

