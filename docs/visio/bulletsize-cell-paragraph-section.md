---
title: Célula BulletSize (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Especifica o tamanho de um marcador.
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771414"
---
# <a name="bulletsize-cell-paragraph-section"></a><span data-ttu-id="54d45-103">Célula BulletSize (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="54d45-103">BulletSize Cell (Paragraph Section)</span></span>

<span data-ttu-id="54d45-104">Especifica o tamanho de um marcador.</span><span class="sxs-lookup"><span data-stu-id="54d45-104">Specifies the size of a bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54d45-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="54d45-105">Remarks</span></span>

<span data-ttu-id="54d45-106">Esse valor pode ser especificado para marcadores predefinidos ou personalizados, como um valor percentual ou específico.</span><span class="sxs-lookup"><span data-stu-id="54d45-106">This value can be specified for either predefined or custom bullets, as either a percentage or a specific value.</span></span> 
  
<span data-ttu-id="54d45-107">Se o valor for zero (0), o marcador é o mesmo tamanho da fonte que do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="54d45-107">If the value is zero (0), the bullet is the same font size as that of the first character in the paragraph.</span></span> <span data-ttu-id="54d45-108">Se o valor é uma porcentagem, o marcador é dimensionado como um percentual do tamanho da fonte do primeiro caractere do parágrafo.</span><span class="sxs-lookup"><span data-stu-id="54d45-108">If the value is a percentage, the bullet is sized as a percentage of the font size of the first character in the paragraph.</span></span> <span data-ttu-id="54d45-109">Números negativos são tratados como porcentagens.</span><span class="sxs-lookup"><span data-stu-id="54d45-109">Negative numbers are treated as percentages.</span></span>
  
<span data-ttu-id="54d45-110">Para obter uma referência à célula BulletSize pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="54d45-110">To get a reference to the BulletSize cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54d45-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="54d45-111">Cell name:</span></span>  <br/> | <span data-ttu-id="54d45-112">Para.BulletFontSize [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="54d45-112">Para.BulletFontSize[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="54d45-113">Para obter uma referência à célula BulletSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="54d45-113">To get a reference to the BulletSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54d45-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="54d45-114">Section index:</span></span>  <br/> |<span data-ttu-id="54d45-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="54d45-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="54d45-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="54d45-116">Row index:</span></span>  <br/> |<span data-ttu-id="54d45-117">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="54d45-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="54d45-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="54d45-118">Cell index:</span></span>  <br/> |<span data-ttu-id="54d45-119">**visBulletFontSize**</span><span class="sxs-lookup"><span data-stu-id="54d45-119">**visBulletFontSize**</span></span> <br/> |
   

