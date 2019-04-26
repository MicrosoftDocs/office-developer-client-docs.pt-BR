---
title: Célula ComplexScriptSize (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359336"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="27a0b-103">Célula ComplexScriptSize (Seção Caracteres)</span><span class="sxs-lookup"><span data-stu-id="27a0b-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="27a0b-104">O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.</span><span class="sxs-lookup"><span data-stu-id="27a0b-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27a0b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="27a0b-105">Remarks</span></span>

<span data-ttu-id="27a0b-106">Tamanhos de fonte de script complexos são listados na guia **Fonte** na caixa de diálogo **Texto** (clique na seta no grupo **Fonte** na guia **Início**).</span><span class="sxs-lookup"><span data-stu-id="27a0b-106">Complex script font sizes   are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="27a0b-107">Essa lista só é exibida se você tiver adicionado um idioma que contenha caracteres Asiáticos ou de script complexo, na caixa de diálogo **Preferências de Idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="27a0b-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="27a0b-108">(Clique em **Iniciar**, em **Todos os programas**, em **Microsoft Office**, em **Ferramentas do Microsoft Office** e em **Preferências de Idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="27a0b-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="27a0b-p102">Você pode inserir esse valor como um tamanho de ponto explícito ou como um percentual. Se você especificar um percentual, o valor é baseado no valor da célula Size. O valor padrão 0 (zero) significa 100%.</span><span class="sxs-lookup"><span data-stu-id="27a0b-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="27a0b-112">Para obter uma referência à célula ComplexScriptSize pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="27a0b-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27a0b-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="27a0b-113">Cell name:</span></span>  <br/> |<span data-ttu-id="27a0b-114">Char.ComplexScriptSize[ *i*  ]           onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="27a0b-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="27a0b-115">Para obter uma referência à célula ComplexScriptSize pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="27a0b-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27a0b-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="27a0b-116">Section index:</span></span>  <br/> |<span data-ttu-id="27a0b-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="27a0b-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="27a0b-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="27a0b-118">Row index:</span></span>  <br/> |<span data-ttu-id="27a0b-119">**visRowCharacter** +  *i*           onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="27a0b-119">**visRowCharacter** +  +  \*\* 
          where *i* = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="27a0b-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="27a0b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="27a0b-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="27a0b-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

