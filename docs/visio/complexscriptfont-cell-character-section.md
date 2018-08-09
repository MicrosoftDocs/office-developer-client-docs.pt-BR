---
title: Célula ComplexScriptFont (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771549"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="e3544-104">Célula ComplexScriptFont (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="e3544-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="e3544-p102">Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="e3544-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3544-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3544-107">Remarks</span></span>

<span data-ttu-id="e3544-108">Tamanhos de fonte de script complexo são listados na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ).</span><span class="sxs-lookup"><span data-stu-id="e3544-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="e3544-109">Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="e3544-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="e3544-110">(Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="e3544-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="e3544-111">O número 0 (zero) significa que nenhuma fonte for especificada.</span><span class="sxs-lookup"><span data-stu-id="e3544-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="e3544-112">A fonte latina ou fontes padrão são usadas.</span><span class="sxs-lookup"><span data-stu-id="e3544-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="e3544-113">Para obter uma referência para a célula ComplexScriptFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e3544-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3544-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e3544-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e3544-115">Char.ComplexScriptFont [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3544-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3544-116">Para obter uma referência para a célula ComplexScriptFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e3544-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3544-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e3544-117">Section index:</span></span>  <br/> |<span data-ttu-id="e3544-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e3544-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="e3544-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e3544-119">Row index:</span></span>  <br/> |<span data-ttu-id="e3544-120">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3544-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e3544-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e3544-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e3544-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="e3544-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

