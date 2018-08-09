---
title: Célula BulletString (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm135
localization_priority: Normal
ms.assetid: 38285824-30ad-0cf2-07cb-0103ab3a415a
description: Permite criar um estilo com marcadores personalizados.
ms.openlocfilehash: bd55e2c061d8e99e0d9e9fd5d9be459b3daae524
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771440"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="0373a-103">Célula BulletString (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="0373a-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="0373a-104">Permite criar um estilo com marcadores personalizados.</span><span class="sxs-lookup"><span data-stu-id="0373a-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0373a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0373a-105">Remarks</span></span>

<span data-ttu-id="0373a-p101">Insira o estilo como uma cadeia de caracteres (entre aspas). Por exemplo, você poderia inserir a cadeia de caracteres: "ooo".</span><span class="sxs-lookup"><span data-stu-id="0373a-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="0373a-108">Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**.</span><span class="sxs-lookup"><span data-stu-id="0373a-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="0373a-109">Para obter uma referência para a célula BulletString pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0373a-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0373a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0373a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="0373a-111">Para.BulletStr [ *i* ] onde *i* = < 1 >, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="0373a-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="0373a-112">Para obter uma referência para a célula BulletString pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0373a-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0373a-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0373a-113">Section index:</span></span>  <br/> |<span data-ttu-id="0373a-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="0373a-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="0373a-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0373a-115">Row index:</span></span>  <br/> |<span data-ttu-id="0373a-116">**visRowParagraph** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="0373a-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="0373a-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0373a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="0373a-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="0373a-118">**visBulletString**</span></span> <br/> |
   

