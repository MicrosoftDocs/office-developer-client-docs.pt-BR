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
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771880"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="bbab3-104">Célula FillPattern (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="bbab3-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="bbab3-p102">Determina o padrão de preenchimento da forma. Para especificar um padrão de preenchimento personalizado, utilize a função USE da célula.</span><span class="sxs-lookup"><span data-stu-id="bbab3-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="bbab3-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bbab3-107">**Value**</span></span>|<span data-ttu-id="bbab3-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bbab3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bbab3-109">0</span><span class="sxs-lookup"><span data-stu-id="bbab3-109">0</span></span>  <br/> |<span data-ttu-id="bbab3-110">Nenhum (preenchimento transparente).</span><span class="sxs-lookup"><span data-stu-id="bbab3-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="bbab3-111">1</span><span class="sxs-lookup"><span data-stu-id="bbab3-111">1</span></span>  <br/> |<span data-ttu-id="bbab3-112">Cor do primeiro plano sólida.</span><span class="sxs-lookup"><span data-stu-id="bbab3-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="bbab3-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="bbab3-113">2 - 40</span></span>  <br/> |<span data-ttu-id="bbab3-114">Padrões de preenchimento variados correspondentes a entradas indexadas na caixa de diálogo **Preenchimento**.</span><span class="sxs-lookup"><span data-stu-id="bbab3-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbab3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbab3-115">Remarks</span></span>

<span data-ttu-id="bbab3-116">Você pode também definir o valor utilizando a caixa de diálogo **Preenchimento** (na guia **Página Inicial**, no grupo **Forma**, clique em **Preenchimento** e em **Opções de preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="bbab3-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="bbab3-117">Para obter uma referência para a célula FillPattern pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="bbab3-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbab3-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bbab3-118">Cell name:</span></span>  <br/> |<span data-ttu-id="bbab3-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="bbab3-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="bbab3-120">Para obter uma referência para a célula FillPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bbab3-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbab3-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bbab3-121">Section index:</span></span>  <br/> |<span data-ttu-id="bbab3-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbab3-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bbab3-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="bbab3-123">Row index:</span></span>  <br/> |<span data-ttu-id="bbab3-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="bbab3-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="bbab3-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="bbab3-125">Cell index:</span></span>  <br/> |<span data-ttu-id="bbab3-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="bbab3-126">**visFillPattern**</span></span> <br/> |
   

