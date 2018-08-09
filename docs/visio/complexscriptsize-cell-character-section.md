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
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771554"
---
# <a name="complexscriptsize-cell-character-section"></a><span data-ttu-id="638a8-103">Célula ComplexScriptSize (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="638a8-103">ComplexScriptSize Cell (Character Section)</span></span>

<span data-ttu-id="638a8-104">O tamanho da fonte utilizada para formatar o texto composto de caracteres de scripts complexos.</span><span class="sxs-lookup"><span data-stu-id="638a8-104">The size of the font used to format text composed of complex script characters.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="638a8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="638a8-105">Remarks</span></span>

<span data-ttu-id="638a8-106">Tamanhos de fonte de script complexo são listados na guia **fonte** da caixa de diálogo **texto** (clique na seta na **fonte** de grupo na guia **página inicial** ).</span><span class="sxs-lookup"><span data-stu-id="638a8-106">Complex script font sizes are listed on the **Font** tab in the **Text** dialog box (click the arrow in the **Font** group on the **Home** tab).</span></span> <span data-ttu-id="638a8-107">Esta lista é exibida somente se você tiver adicionado um idioma que contém caracteres asiáticos ou de script complexo, na caixa de diálogo **Preferências de idioma do Microsoft Office** .</span><span class="sxs-lookup"><span data-stu-id="638a8-107">This list appears only if you have added a language that contains Asian or complex script characters, in the **Microsoft Office Language Preferences** dialog box.</span></span> <span data-ttu-id="638a8-108">(Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="638a8-108">(Click **Start**, click **All Programs**, click **Microsoft Office**, click **Microsoft Office Tools**, and then click **Microsoft Office Language Preferences**.</span></span>
  
<span data-ttu-id="638a8-p102">Você pode inserir esse valor como um tamanho de ponto explícito ou como um percentual. Se você especificar um percentual, o valor é baseado no valor da célula Size. O valor padrão 0 (zero) significa 100%.</span><span class="sxs-lookup"><span data-stu-id="638a8-p102">You can enter this value as an explicit point size or as a percentage. If you specify a percentage, the value is based on the value in the Size cell. A default value of 0 (zero) means 100%.</span></span> 
  
<span data-ttu-id="638a8-112">Para obter uma referência para a célula ComplexScriptFont pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="638a8-112">To get a reference to the ComplexScriptSize cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="638a8-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="638a8-113">Cell name:</span></span>  <br/> |<span data-ttu-id="638a8-114">Char.ComplexScriptSize [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="638a8-114">Char.ComplexScriptSize[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="638a8-115">Para obter uma referência para a célula ComplexScriptSize pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="638a8-115">To get a reference to the ComplexScriptSize cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="638a8-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="638a8-116">Section index:</span></span>  <br/> |<span data-ttu-id="638a8-117">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="638a8-117">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="638a8-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="638a8-118">Row index:</span></span>  <br/> |<span data-ttu-id="638a8-119">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="638a8-119">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="638a8-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="638a8-120">Cell index:</span></span>  <br/> |<span data-ttu-id="638a8-121">**visCharacterComplexScriptSize**</span><span class="sxs-lookup"><span data-stu-id="638a8-121">**visCharacterComplexScriptSize**</span></span> <br/> |
   

