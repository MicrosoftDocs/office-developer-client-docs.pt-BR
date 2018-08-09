---
title: Célula ShdwForegndTrans (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Determina o nível de transparência para a cor utilizada para o primeiro plano (traço) do padrão de preenchimento da sombra projetada da forma.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772940"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="73254-103">Célula ShdwForegndTrans (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="73254-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="73254-104">Determina o nível de transparência para a cor utilizada para o primeiro plano (traço) do padrão de preenchimento da sombra projetada da forma.</span><span class="sxs-lookup"><span data-stu-id="73254-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="73254-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="73254-105">**Value**</span></span>|<span data-ttu-id="73254-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="73254-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73254-107">
          0 - 100
</span><span class="sxs-lookup"><span data-stu-id="73254-107">0 - 100</span></span>  <br/> |<span data-ttu-id="73254-p101">Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="73254-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73254-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="73254-110">Remarks</span></span>

<span data-ttu-id="73254-111">Valores são arredondados para o meio por cento mais próximo.</span><span class="sxs-lookup"><span data-stu-id="73254-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="73254-112">Um valor de 100% é completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="73254-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="73254-113">Embora uma sombra com preenchimento completamente transparente aparece na página de desenho da mesma como uma sombra que não tenha preenchimento, ele se interage com outros objetos na página da mesma forma como se a transparência fosse 0%.</span><span class="sxs-lookup"><span data-stu-id="73254-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="73254-p103">Você pode também definir o valor utilizando o controle deslizante na caixa de diálogo **Sombra** (na guia **Página Inicial**, no grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**). Esse valor controla o valor das transparências de sombra do primeiro plano e do plano de fundo. Para definir os valores independentemente, insira-os na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="73254-p103">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**). This value controls the value of both the background and foreground shadow transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="73254-117">Para obter uma referência para a célula ShdwForegndTrans pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="73254-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73254-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="73254-118">Cell name:</span></span>  <br/> |<span data-ttu-id="73254-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="73254-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="73254-120">Para obter uma referência para a célula ShdwForegndTrans pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="73254-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73254-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="73254-121">Section index:</span></span>  <br/> |<span data-ttu-id="73254-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="73254-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="73254-123">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="73254-123">Row index:</span></span>  <br/> |<span data-ttu-id="73254-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="73254-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="73254-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="73254-125">Cell index:</span></span>  <br/> |<span data-ttu-id="73254-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="73254-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

