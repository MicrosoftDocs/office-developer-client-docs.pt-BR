---
title: Célula LockFromGroupFormat (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359588"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="9dd24-102">Célula LockFromGroupFormat (Seção Proteção)</span><span class="sxs-lookup"><span data-stu-id="9dd24-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="9dd24-103">Bloqueia alterações no formato de uma forma de grupo para serem propagadas para suas subformas, enquanto ainda permite que os usuários formatem as subformas selecionadas diretamente.</span><span class="sxs-lookup"><span data-stu-id="9dd24-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="9dd24-104">O valor da célula LockFromGroupFormat corresponde à configuração da caixa de seleção **De formatação de grupo** na caixa de diálogo **Proteção**.</span><span class="sxs-lookup"><span data-stu-id="9dd24-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="9dd24-105">Para referir-se à célula LockFromGroupFormat pelo nome de outra fórmula, ou a partir de um programa, usando a propriedade **CellsU**, utilize:

</span><span class="sxs-lookup"><span data-stu-id="9dd24-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9dd24-106">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="9dd24-106">Cell name:</span></span>  <br/> |<span data-ttu-id="9dd24-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="9dd24-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="9dd24-108">Para referir-se à célula LockFromGroupFormat pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="9dd24-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9dd24-109">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="9dd24-109">Section index:</span></span>  <br/> |<span data-ttu-id="9dd24-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9dd24-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9dd24-111">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="9dd24-111">Row index:</span></span>  <br/> |<span data-ttu-id="9dd24-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9dd24-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="9dd24-113">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="9dd24-113">Cell index:</span></span>  <br/> |<span data-ttu-id="9dd24-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="9dd24-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="9dd24-115">O valor padrão da célula é 0 (False).</span><span class="sxs-lookup"><span data-stu-id="9dd24-115">The default value for the cell is 0 (False).</span></span>
  

