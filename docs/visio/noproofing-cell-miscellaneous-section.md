---
title: Célula NoProofing (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina se a ortografia será corrigida automaticamente e se erros de ortografia serão exibidos para a forma selecionada. Aceita um valor Boolean.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431250"
---
# <a name="noproofing-cell-miscellaneous-section"></a><span data-ttu-id="02500-104">Célula NoProofing (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="02500-104">NoProofing Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="02500-105">Determina se a ortografia será corrigida automaticamente e se erros de ortografia serão exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="02500-105">Determines whether spelling is automatically corrected and whether spelling errors are displayed for the selected shape.</span></span> <span data-ttu-id="02500-106">Aceita um **valor Boolean.**</span><span class="sxs-lookup"><span data-stu-id="02500-106">Takes a **Boolean** value.</span></span> 
  
|<span data-ttu-id="02500-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="02500-107">**Value**</span></span>|<span data-ttu-id="02500-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02500-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02500-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="02500-109">TRUE</span></span>  <br/> |<span data-ttu-id="02500-110">A ortografia não é corrigida automaticamente e os erros de ortografia não são exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="02500-110">Spelling is not automatically corrected and spelling errors are not displayed for the selected shape.</span></span>  <br/> |
|<span data-ttu-id="02500-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="02500-111">FALSE</span></span>  <br/> |<span data-ttu-id="02500-112">A ortografia é corrigida automaticamente e os erros de ortografia são exibidos para a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="02500-112">Spelling is automatically corrected and spelling errors are displayed for the selected shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02500-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="02500-113">Remarks</span></span>

<span data-ttu-id="02500-114">Para fazer referência à célula NoProofing pelo nome, a partir de outra fórmula ou programa, usando a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="02500-114">To get a reference to the NoProofing cell by name from another formula or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02500-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="02500-115">Cell name:</span></span>  <br/> |<span data-ttu-id="02500-116">NoProofing</span><span class="sxs-lookup"><span data-stu-id="02500-116">NoProofing</span></span>  <br/> |
   
<span data-ttu-id="02500-117">Para fazer referência à célula NoProofing pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="02500-117">To get a reference to the NoProofing cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02500-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="02500-118">Section index:</span></span>  <br/> |<span data-ttu-id="02500-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02500-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="02500-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="02500-120">Row index:</span></span>  <br/> |<span data-ttu-id="02500-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="02500-121">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="02500-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="02500-122">Cell index:</span></span>  <br/> |<span data-ttu-id="02500-123">**visObjNoProofing**</span><span class="sxs-lookup"><span data-stu-id="02500-123">**visObjNoProofing**</span></span> <br/> |
   

