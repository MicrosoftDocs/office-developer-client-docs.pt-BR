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
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404831"
---
# <a name="complexscriptfont-cell-character-section"></a><span data-ttu-id="7fa9c-104">Célula ComplexScriptFont (Seção Caractere)</span><span class="sxs-lookup"><span data-stu-id="7fa9c-104">ComplexScriptFont Cell (Character Section)</span></span>

<span data-ttu-id="7fa9c-p102">Contém o número da fonte utilizada para formatar o texto composto de caracteres de script complexos. Os números de fonte variam de acordo com as fontes instaladas em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="7fa9c-p102">Contains the number of the font used to format text composed of complex script characters. Font numbers vary according to the fonts installed on your system.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7fa9c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fa9c-107">Remarks</span></span>

<span data-ttu-id="7fa9c-108">Tamanhos de fonte de script complexos são listados na guia **Fonte** na caixa de diálogo **Texto** (clique na seta no grupo **Fonte** na guia **Início**).</span><span class="sxs-lookup"><span data-stu-id="7fa9c-108">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="7fa9c-109">Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="7fa9c-109">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="7fa9c-110">(Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="7fa9c-110">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="7fa9c-111">O número 0 (zero) significa que não há fontes especificadas.</span><span class="sxs-lookup"><span data-stu-id="7fa9c-111">The number 0 (zero) means no font is specified.</span></span> <span data-ttu-id="7fa9c-112">A fonte latina ou fontes padrão são usadas.</span><span class="sxs-lookup"><span data-stu-id="7fa9c-112">The Latin font or default fonts are used.</span></span>
  
<span data-ttu-id="7fa9c-113">Para obter uma referência à célula ComplexScriptSize pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-113">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fa9c-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7fa9c-115">Char.ComplexScriptFont[ *i*  ]           onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7fa9c-115">Char.ComplexScriptFont[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7fa9c-116">Para obter uma referência à célula ComplexScriptFont pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-116">To get a reference to the ComplexScriptFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fa9c-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-117">Section index:</span></span>  <br/> |<span data-ttu-id="7fa9c-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7fa9c-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="7fa9c-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-119">Row index:</span></span>  <br/> |<span data-ttu-id="7fa9c-120">**visRowCharacter** +  *i*           onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7fa9c-120">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7fa9c-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="7fa9c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7fa9c-122">**visCharacterComplexScriptFont**</span><span class="sxs-lookup"><span data-stu-id="7fa9c-122">**visCharacterComplexScriptFont**</span></span> <br/> |
   

