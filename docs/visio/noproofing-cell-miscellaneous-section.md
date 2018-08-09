---
title: Célula NoProofing (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina a ortografia foi corrigida automaticamente e se os erros de ortografia são exibidos para a forma selecionada. Recebe um valor booleano.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19772416"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="8145a-104">Célula NoProofing (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="8145a-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="8145a-105">Determina a ortografia foi corrigida automaticamente e se os erros de ortografia são exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="8145a-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="8145a-106">Recebe um valor **booleano** .</span><span class="sxs-lookup"><span data-stu-id="8145a-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="8145a-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8145a-107">**Value**</span></span>|<span data-ttu-id="8145a-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8145a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8145a-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="8145a-109">TRUE</span></span>  <br/> |<span data-ttu-id="8145a-110">Ortografia automaticamente não for corrigida e erros de ortografia não são exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="8145a-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="8145a-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="8145a-111">FALSE</span></span>  <br/> |<span data-ttu-id="8145a-112">Corrigidas automaticamente de ortografia e erros de ortografia são exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="8145a-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8145a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8145a-113">Remarks</span></span>

<span data-ttu-id="8145a-114">Para obter uma referência à célula NoProofing pelo nome, a partir de outra fórmula ou de um programa, usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="8145a-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8145a-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8145a-115">Cell name:</span></span>  <br/> |<span data-ttu-id="8145a-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="8145a-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="8145a-117">Para obter uma referência à célula NoProofing pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8145a-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8145a-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8145a-118">Section index:</span></span>  <br/> |<span data-ttu-id="8145a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8145a-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8145a-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8145a-120">Row index:</span></span>  <br/> |<span data-ttu-id="8145a-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="8145a-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="8145a-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8145a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="8145a-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="8145a-123">**visObjNoProofing**</span></span> <br/> |
   

