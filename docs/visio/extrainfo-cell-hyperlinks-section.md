---
title: Célula ExtraInfo (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Representa uma sequência de caracteres que passa as informações que serão utilizadas para resolver um URL, como as coordenadas de um mapa de imagens. Por exemplo, na célula ExtraInfo, x = 41&amp;y = 7specifies as coordenadas de um mapa de imagem.
ms.openlocfilehash: df2886ef7911b484cc60e8a476bfa53369fbf646
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357817"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="fd2a7-104">Célula ExtraInfo (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="fd2a7-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="fd2a7-105">Representa uma sequência de caracteres que passa as informações que serão utilizadas para resolver um URL, como as coordenadas de um mapa de imagens.</span><span class="sxs-lookup"><span data-stu-id="fd2a7-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="fd2a7-106">Por exemplo, na célula ExtraInfo, "x = 41&amp;y = 7" especifica as coordenadas de um mapa de imagem.</span><span class="sxs-lookup"><span data-stu-id="fd2a7-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd2a7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd2a7-107">Remarks</span></span>

<span data-ttu-id="fd2a7-108">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="fd2a7-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="fd2a7-109">Para fazer referência à célula ExtraInfo pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd2a7-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fd2a7-111">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="fd2a7-111">Hyperlink.</span></span>  <span data-ttu-id="fd2a7-112">*nome* . ExtraInfo onde hiperlink.</span><span class="sxs-lookup"><span data-stu-id="fd2a7-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="fd2a7-113">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="fd2a7-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="fd2a7-114">Para fazer referência à célula ExtraInfo pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd2a7-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-115">Section index:</span></span>  <br/> |<span data-ttu-id="fd2a7-116">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="fd2a7-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="fd2a7-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-117">Row index:</span></span>  <br/> |<span data-ttu-id="fd2a7-118">**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fd2a7-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="fd2a7-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="fd2a7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="fd2a7-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="fd2a7-120">**visHLinkExtraInfo**</span></span> <br/> |
   

