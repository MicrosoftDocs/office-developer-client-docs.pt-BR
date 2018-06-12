---
title: Célula ShdwForegnd (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Determina a cor utilizada para o primeiro plano (traço) do padrão de preenchimento de sombra projetada da forma.
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772954"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="87351-103">Célula ShdwForegnd (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="87351-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="87351-104">Determina a cor utilizada para o primeiro plano (traço) do padrão de preenchimento de sombra projetada da forma.</span><span class="sxs-lookup"><span data-stu-id="87351-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87351-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="87351-105">Remarks</span></span>

<span data-ttu-id="87351-106">Para definir a cor, insira um número de 0 a 23, que serve como um índice para uma coleção de cores.</span><span class="sxs-lookup"><span data-stu-id="87351-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="87351-107">Para inserir uma cor personalizada, use a função RGB ou HSL.</span><span class="sxs-lookup"><span data-stu-id="87351-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="87351-108">O valor de uma cor personalizada é a cor RGB e RGB ( *r, g, b*), em vez de um número, será exibido na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="87351-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="87351-109">Quando usado em operações numéricas, as cores têm valores de 24 e acima.</span><span class="sxs-lookup"><span data-stu-id="87351-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="87351-110">É possível definir a transparência da cor do primeiro plano do padrão de preenchimento da sombra projetada da forma na célula ShdwForegndTrans.</span><span class="sxs-lookup"><span data-stu-id="87351-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="87351-111">Para obter uma referência para a célula ShdwForegnd pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="87351-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87351-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="87351-112">Cell name:</span></span>  <br/> | <span data-ttu-id="87351-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="87351-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="87351-114">Para obter uma referência para a célula ShdwForegnd pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="87351-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87351-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="87351-115">Section index:</span></span>  <br/> |<span data-ttu-id="87351-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87351-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="87351-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="87351-117">Row index:</span></span>  <br/> |<span data-ttu-id="87351-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="87351-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="87351-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="87351-119">Cell index:</span></span>  <br/> |<span data-ttu-id="87351-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="87351-120">**visFillShdwForegnd**</span></span> <br/> |
   

