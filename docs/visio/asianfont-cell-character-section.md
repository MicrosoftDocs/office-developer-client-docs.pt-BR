---
title: Célula AsianFont (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771270"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="ab0b3-104">Célula AsianFont (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="ab0b3-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="ab0b3-p102">Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="ab0b3-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ab0b3-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab0b3-107">Remarks</span></span>

<span data-ttu-id="ab0b3-108">Fontes para idiomas asiáticos são listadas na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ).</span><span class="sxs-lookup"><span data-stu-id="ab0b3-108">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="ab0b3-109">Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="ab0b3-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="ab0b3-110">(Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="ab0b3-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="ab0b3-p104">O número 0 significa que não há fontes especificadas. A fonte latina ou as fontes padrão são usadas se elas contiverem os caracteres necessários.</span><span class="sxs-lookup"><span data-stu-id="ab0b3-p104">The number 0 means no font is specified. The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="ab0b3-113">Para obter uma referência à célula AsianFont pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab0b3-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-114">Cell name:</span></span>  <br/> |<span data-ttu-id="ab0b3-115">Char.AsianFont [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ab0b3-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ab0b3-116">Para obter uma referência à célula AsianFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab0b3-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-117">Section index:</span></span>  <br/> |<span data-ttu-id="ab0b3-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="ab0b3-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="ab0b3-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-119">Row index:</span></span>  <br/> |<span data-ttu-id="ab0b3-120">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ab0b3-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="ab0b3-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ab0b3-121">Cell index:</span></span>  <br/> |<span data-ttu-id="ab0b3-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="ab0b3-122">**visCharacterAsianFont**</span></span> <br/> |
   

