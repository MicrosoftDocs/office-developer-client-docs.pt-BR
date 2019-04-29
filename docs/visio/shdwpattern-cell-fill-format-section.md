---
title: Célula ShdwPattern (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Determina o padrão de preenchimento da sombra de uma forma.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427609"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="0b757-103">Célula ShdwPattern (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="0b757-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="0b757-104">Determina o padrão de preenchimento da sombra de uma forma.</span><span class="sxs-lookup"><span data-stu-id="0b757-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="0b757-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0b757-105">**Value**</span></span>|<span data-ttu-id="0b757-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b757-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b757-107">,0</span><span class="sxs-lookup"><span data-stu-id="0b757-107">0</span></span>  <br/> |<span data-ttu-id="0b757-108">Nenhum (preenchimento transparente)</span><span class="sxs-lookup"><span data-stu-id="0b757-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="0b757-109">1</span><span class="sxs-lookup"><span data-stu-id="0b757-109">1</span></span>  <br/> |<span data-ttu-id="0b757-110">Cor do primeiro plano sólida</span><span class="sxs-lookup"><span data-stu-id="0b757-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="0b757-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="0b757-111">2 - 40</span></span>  <br/> |<span data-ttu-id="0b757-112">Padrões variados</span><span class="sxs-lookup"><span data-stu-id="0b757-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b757-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b757-113">Remarks</span></span>

<span data-ttu-id="0b757-p101">Para definir o padrão de preenchimento, insira um número de 0 a 40, que serve como um índice para uma coleção de padrões. É possível visualizar a coleção de padrões de preenchimento na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, do grupo **Forma**, clique em **Preenchimento** e em **Opções de Preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="0b757-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="0b757-116">Para obter uma referência para a célula ShdwPattern pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0b757-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b757-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0b757-117">Cell name:</span></span>  <br/> |<span data-ttu-id="0b757-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="0b757-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="0b757-119">Para obter uma referência para a célula ShdwPattern pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0b757-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b757-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0b757-120">Section index:</span></span>  <br/> |<span data-ttu-id="0b757-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b757-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0b757-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="0b757-122">Row index:</span></span>  <br/> |<span data-ttu-id="0b757-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0b757-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="0b757-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0b757-124">Cell index:</span></span>  <br/> |<span data-ttu-id="0b757-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="0b757-125">**visFillShdwPattern**</span></span> <br/> |
   

