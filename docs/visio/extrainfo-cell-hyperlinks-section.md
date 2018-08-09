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
description: Representa uma cadeia de caracteres que passa informações a serem usadas na resolução de uma URL, como as coordenadas de um mapa de imagem. Por exemplo, na célula ExtraInfo, x = 41&amp;y = 7specifies as coordenadas de um mapa de imagem.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771847"
---
# <a name="extrainfo-cell-hyperlinks-section"></a><span data-ttu-id="8e60a-104">Célula ExtraInfo (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="8e60a-104">ExtraInfo Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="8e60a-105">Representa uma cadeia de caracteres que passa informações a serem usadas na resolução de uma URL, como as coordenadas de um mapa de imagem.</span><span class="sxs-lookup"><span data-stu-id="8e60a-105">Represents a string that passes information to be used in resolving a URL, such as the coordinates of an image map.</span></span> <span data-ttu-id="8e60a-106">Por exemplo, na célula ExtraInfo, "x = 41&amp;y = 7" Especifica as coordenadas de um mapa de imagem.</span><span class="sxs-lookup"><span data-stu-id="8e60a-106">For example, in the ExtraInfo cell, "x=41&amp;y=7" specifies the coordinates of an image map.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e60a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e60a-107">Remarks</span></span>

<span data-ttu-id="8e60a-108">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="8e60a-108">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="8e60a-109">Para fazer referência à célula ExtraInfo pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8e60a-109">To get a reference to the ExtraInfo cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e60a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8e60a-110">Cell name:</span></span>  <br/> | <span data-ttu-id="8e60a-111">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="8e60a-111">Hyperlink.</span></span>  <span data-ttu-id="8e60a-112">*nome* . ExtraInfo onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="8e60a-112">*name*  .ExtraInfo            where Hyperlink.</span></span>  <span data-ttu-id="8e60a-113">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="8e60a-113">*name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="8e60a-114">Para fazer referência à célula ExtraInfo pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8e60a-114">To get a reference to the ExtraInfo cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8e60a-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8e60a-115">Section index:</span></span>  <br/> |<span data-ttu-id="8e60a-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="8e60a-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="8e60a-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8e60a-117">Row index:</span></span>  <br/> |<span data-ttu-id="8e60a-118">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8e60a-118">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8e60a-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8e60a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="8e60a-120">**visHLinkExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="8e60a-120">**visHLinkExtraInfo**</span></span> <br/> |
   

