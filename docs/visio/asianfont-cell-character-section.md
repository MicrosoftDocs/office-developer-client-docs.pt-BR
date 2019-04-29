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
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406588"
---
# <a name="asianfont-cell-character-section"></a><span data-ttu-id="fcb4a-104">Célula AsianFont (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="fcb4a-104">AsianFont Cell (Character Section)</span></span>

<span data-ttu-id="fcb4a-p102">Contém o número da fonte utilizada para formatar o texto com caracteres asiáticos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="fcb4a-p102">Contains the number of the font used to format the text containing Asian characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fcb4a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcb4a-107">Remarks</span></span>

<span data-ttu-id="fcb4a-p103">Fontes asiáticas são listadas na guia **Fonte** na caixa de diálogo **Texto** (clique na seta do grupo **Fonte** na guia **Página Inicial**). Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**. (Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="fcb4a-p103">Asian fonts are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab). This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box. (Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="fcb4a-111">O número 0 significa que não há fontes especificadas.</span><span class="sxs-lookup"><span data-stu-id="fcb4a-111">The number 0 means no font is specified.</span></span> <span data-ttu-id="fcb4a-112">A fonte latina ou as fontes padrão são usadas se elas contiverem os caracteres necessários.</span><span class="sxs-lookup"><span data-stu-id="fcb4a-112">The Latin font or default fonts are used if they contain the necessary characters.</span></span>
  
<span data-ttu-id="fcb4a-113">Para fazer referência à célula AsianFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-113">To get a reference to the AsianFont cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb4a-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="fcb4a-115">Char. AsianFont [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="fcb4a-115">Char.AsianFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="fcb4a-116">Para fazer referência à célula AsianFont pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-116">To get a reference to the AsianFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb4a-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-117">Section index:</span></span>  <br/> |<span data-ttu-id="fcb4a-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="fcb4a-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="fcb4a-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-119">Row index:</span></span>  <br/> |<span data-ttu-id="fcb4a-120">**visRowCharacter** +  *i*           onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fcb4a-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fcb4a-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="fcb4a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="fcb4a-122">**visCharacterAsianFont**</span><span class="sxs-lookup"><span data-stu-id="fcb4a-122">**visCharacterAsianFont**</span></span> <br/> |
   

