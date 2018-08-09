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
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772947"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="1b97b-103">Célula ShdwPattern (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="1b97b-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="1b97b-104">Determina o padrão de preenchimento da sombra de uma forma.</span><span class="sxs-lookup"><span data-stu-id="1b97b-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="1b97b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1b97b-105">**Value**</span></span>|<span data-ttu-id="1b97b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b97b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b97b-107">0</span><span class="sxs-lookup"><span data-stu-id="1b97b-107">0</span></span>  <br/> |<span data-ttu-id="1b97b-108">Nenhum (preenchimento transparente)</span><span class="sxs-lookup"><span data-stu-id="1b97b-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="1b97b-109">1</span><span class="sxs-lookup"><span data-stu-id="1b97b-109">1</span></span>  <br/> |<span data-ttu-id="1b97b-110">Cor do primeiro plano sólida</span><span class="sxs-lookup"><span data-stu-id="1b97b-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="1b97b-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="1b97b-111">2 - 40</span></span>  <br/> |<span data-ttu-id="1b97b-112">Padrões variados</span><span class="sxs-lookup"><span data-stu-id="1b97b-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b97b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b97b-113">Remarks</span></span>

<span data-ttu-id="1b97b-p101">Para definir o padrão de preenchimento, insira um número de 0 a 40, que serve como um índice para uma coleção de padrões. É possível visualizar a coleção de padrões de preenchimento na caixa de diálogo **Preenchimento** (na guia **Página Inicial**, do grupo **Forma**, clique em **Preenchimento** e em **Opções de Preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="1b97b-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="1b97b-116">Para obter uma referência para a célula ShdwPattern pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1b97b-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b97b-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1b97b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="1b97b-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="1b97b-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="1b97b-119">Para obter uma referência para a célula ShdwPattern pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1b97b-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b97b-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1b97b-120">Section index:</span></span>  <br/> |<span data-ttu-id="1b97b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1b97b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1b97b-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1b97b-122">Row index:</span></span>  <br/> |<span data-ttu-id="1b97b-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="1b97b-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="1b97b-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1b97b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="1b97b-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="1b97b-125">**visFillShdwPattern**</span></span> <br/> |
   

