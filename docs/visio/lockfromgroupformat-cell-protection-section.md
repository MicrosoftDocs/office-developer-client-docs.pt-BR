---
title: Célula LockFromGroupFormat (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426055"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="f0784-102">Célula LockFromGroupFormat (Seção Proteção)</span><span class="sxs-lookup"><span data-stu-id="f0784-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="f0784-103">Impede que as alterações de formato em uma forma de grupo seja propagada para suas sub formas, enquanto ainda permite que os usuários forndem sub formas selecionadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="f0784-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="f0784-104">O valor da célula LockFromGroupFormat corresponde à configuração da caixa de seleção **De formatação de grupo** na caixa de diálogo **Proteção**.</span><span class="sxs-lookup"><span data-stu-id="f0784-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="f0784-105">Para referir-se à célula LockFromGroupFormat pelo nome de outra fórmula, ou a partir de um programa, usando a propriedade **CellsU**, utilize:

</span><span class="sxs-lookup"><span data-stu-id="f0784-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0784-106">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f0784-106">Cell name:</span></span>  <br/> |<span data-ttu-id="f0784-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="f0784-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="f0784-108">Para referir-se à célula LockFromGroupFormat pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f0784-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0784-109">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f0784-109">Section index:</span></span>  <br/> |<span data-ttu-id="f0784-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0784-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f0784-111">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f0784-111">Row index:</span></span>  <br/> |<span data-ttu-id="f0784-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f0784-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="f0784-113">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="f0784-113">Cell index:</span></span>  <br/> |<span data-ttu-id="f0784-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="f0784-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="f0784-115">O valor padrão da célula é 0 (False).</span><span class="sxs-lookup"><span data-stu-id="f0784-115">The default value for the cell is 0 (False).</span></span>
  

