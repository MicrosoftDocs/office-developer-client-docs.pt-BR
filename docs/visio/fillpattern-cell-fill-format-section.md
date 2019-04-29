---
title: Célula FillPattern (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422926"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="a9c38-104">Célula FillPattern (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="a9c38-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="a9c38-105">Determina o padrão de preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="a9c38-105">Determines the fill pattern for the shape.</span></span> <span data-ttu-id="a9c38-106">Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.</span><span class="sxs-lookup"><span data-stu-id="a9c38-106">To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="a9c38-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a9c38-107">**Value**</span></span>|<span data-ttu-id="a9c38-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a9c38-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a9c38-109">,0</span><span class="sxs-lookup"><span data-stu-id="a9c38-109">0</span></span>  <br/> |<span data-ttu-id="a9c38-110">Nenhum (preenchimento transparente).</span><span class="sxs-lookup"><span data-stu-id="a9c38-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="a9c38-111">1</span><span class="sxs-lookup"><span data-stu-id="a9c38-111">1</span></span>  <br/> |<span data-ttu-id="a9c38-112">Cor do primeiro plano sólida.</span><span class="sxs-lookup"><span data-stu-id="a9c38-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="a9c38-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="a9c38-113">2 - 40</span></span>  <br/> |<span data-ttu-id="a9c38-114">Padrões de preenchimento variados correspondentes a entradas indexadas na caixa de diálogo **Preenchimento**.</span><span class="sxs-lookup"><span data-stu-id="a9c38-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9c38-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9c38-115">Remarks</span></span>

<span data-ttu-id="a9c38-116">Você pode também definir o valor utilizando a caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="a9c38-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="a9c38-117">Para obter uma referência para a célula FillPattern pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a9c38-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9c38-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a9c38-118">Cell name:</span></span>  <br/> |<span data-ttu-id="a9c38-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="a9c38-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="a9c38-120">Para obter uma referência para a célula FillPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a9c38-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9c38-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a9c38-121">Section index:</span></span>  <br/> |<span data-ttu-id="a9c38-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9c38-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a9c38-123">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="a9c38-123">Row index:</span></span>  <br/> |<span data-ttu-id="a9c38-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="a9c38-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="a9c38-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a9c38-125">Cell index:</span></span>  <br/> |<span data-ttu-id="a9c38-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="a9c38-126">**visFillPattern**</span></span> <br/> |
   

