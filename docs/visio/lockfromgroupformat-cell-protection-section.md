---
title: Célula LockFromGroupFormat (Seção Proteção)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772260"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="b691b-102">Célula LockFromGroupFormat (Seção Proteção)</span><span class="sxs-lookup"><span data-stu-id="b691b-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="b691b-103">Blocos de formato alterações a uma forma de grupo sejam propagadas para suas subformas enquanto ainda permite que os usuários formatar as formas selecionadas sub-recurso diretamente.</span><span class="sxs-lookup"><span data-stu-id="b691b-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="b691b-104">O valor da célula LockFromGroupFormat corresponde à configuração da caixa de seleção **de formatação de grupo** na caixa de diálogo **proteção** .</span><span class="sxs-lookup"><span data-stu-id="b691b-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="b691b-105">Para fazer referência à célula LockFromGroupFormat pelo nome, a partir de outra fórmula ou de um programa, use a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b691b-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b691b-106">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b691b-106">Cell name:</span></span>  <br/> |<span data-ttu-id="b691b-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="b691b-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="b691b-108">Para fazer referência à célula LockFromGroupFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b691b-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b691b-109">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b691b-109">Section index:</span></span>  <br/> |<span data-ttu-id="b691b-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b691b-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b691b-111">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b691b-111">Row index:</span></span>  <br/> |<span data-ttu-id="b691b-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="b691b-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="b691b-113">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b691b-113">Cell index:</span></span>  <br/> |<span data-ttu-id="b691b-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="b691b-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="b691b-115">O valor padrão da célula é 0 (False).</span><span class="sxs-lookup"><span data-stu-id="b691b-115">The default value for the cell is 0 (False).</span></span>
  

