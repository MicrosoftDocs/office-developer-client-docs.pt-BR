---
title: Célula LockReplace (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772253"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="66a8c-103">Célula LockReplace (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="66a8c-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="66a8c-104">Indica se uma forma pode participar de uma operação de substituição (como um destino ou uma forma de substituição).</span><span class="sxs-lookup"><span data-stu-id="66a8c-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="66a8c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="66a8c-105">**Value**</span></span>|<span data-ttu-id="66a8c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="66a8c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66a8c-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="66a8c-107">TRUE</span></span>  <br/> |<span data-ttu-id="66a8c-108">A forma não pode ser substituída ou a ser usada como uma forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="66a8c-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="66a8c-109">Para uma forma na tela de desenho, o botão **Alterar forma** é desabilitado quando a forma é selecionada.</span><span class="sxs-lookup"><span data-stu-id="66a8c-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="66a8c-110">Para uma forma em um estêncil, a forma não é exibido como uma forma de substituição quando o botão **Alterar forma** for clicado.</span><span class="sxs-lookup"><span data-stu-id="66a8c-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="66a8c-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="66a8c-111">FALSE</span></span>  <br/> |<span data-ttu-id="66a8c-112">A forma pode ser substituída ou usada como uma forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="66a8c-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66a8c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a8c-113">Remarks</span></span>

<span data-ttu-id="66a8c-114">Para fazer referência à célula **LockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="66a8c-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66a8c-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="66a8c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="66a8c-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="66a8c-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="66a8c-117">Para obter uma referência à célula **LockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="66a8c-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="66a8c-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="66a8c-118">Section index:</span></span>  <br/> |<span data-ttu-id="66a8c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="66a8c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="66a8c-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="66a8c-120">Row index:</span></span>  <br/> |<span data-ttu-id="66a8c-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="66a8c-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="66a8c-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="66a8c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="66a8c-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="66a8c-123">**visLockReplace**</span></span> <br/> |
   

