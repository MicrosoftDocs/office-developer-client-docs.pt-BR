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
ms.openlocfilehash: b7a1d7f845c7b9945670240361a4ac66efa80786
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337559"
---
# <a name="bulletstring-cell-paragraph-section"></a><span data-ttu-id="7075e-103">Célula BulletString (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="7075e-103">BulletString Cell (Paragraph Section)</span></span>

<span data-ttu-id="7075e-104">Permite criar um estilo com marcadores personalizados.</span><span class="sxs-lookup"><span data-stu-id="7075e-104">Allows you to create a custom bullet style.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7075e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="7075e-105">Remarks</span></span>

<span data-ttu-id="7075e-p101">Insira o estilo como uma cadeia de caracteres (entre aspas). Por exemplo, você poderia inserir a cadeia de caracteres: "ooo".</span><span class="sxs-lookup"><span data-stu-id="7075e-p101">Enter the style as a string (within quotation marks). For example, you could enter the string, "ooo."</span></span>
  
<span data-ttu-id="7075e-108">Também é possível definir o valor desta célula clicando com o botão direito do mouse em uma forma, apontando para **Formatar**, clicando em **Texto** e na guia **Marcadores**.</span><span class="sxs-lookup"><span data-stu-id="7075e-108">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="7075e-109">Para obter uma referência para a célula BulletString pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7075e-109">To get a reference to the BulletString cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7075e-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7075e-110">Cell name:</span></span>  <br/> |<span data-ttu-id="7075e-111">Para. BulletStr [ *i* ] onde *i* = <1>, 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="7075e-111">Para.BulletStr[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="7075e-112">Para obter uma referência para a célula BulletString pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7075e-112">To get a reference to the BulletString cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7075e-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7075e-113">Section index:</span></span>  <br/> |<span data-ttu-id="7075e-114">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7075e-114">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="7075e-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7075e-115">Row index:</span></span>  <br/> |<span data-ttu-id="7075e-116">**visRowParagraph** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="7075e-116">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="7075e-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7075e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="7075e-118">**visBulletString**</span><span class="sxs-lookup"><span data-stu-id="7075e-118">**visBulletString**</span></span> <br/> |
   

