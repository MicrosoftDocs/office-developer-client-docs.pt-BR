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
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="0af66-103">Célula ShdwPattern (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="0af66-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="0af66-104">Determina o padrão de preenchimento da sombra de uma forma.</span><span class="sxs-lookup"><span data-stu-id="0af66-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="0af66-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0af66-105">**Value**</span></span>|<span data-ttu-id="0af66-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0af66-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0af66-107">0</span><span class="sxs-lookup"><span data-stu-id="0af66-107">0</span></span>  <br/> |<span data-ttu-id="0af66-108">Nenhum (preenchimento transparente)</span><span class="sxs-lookup"><span data-stu-id="0af66-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="0af66-109">1</span><span class="sxs-lookup"><span data-stu-id="0af66-109">1</span></span>  <br/> |<span data-ttu-id="0af66-110">Cor do primeiro plano sólida</span><span class="sxs-lookup"><span data-stu-id="0af66-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="0af66-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="0af66-111">2 - 40</span></span>  <br/> |<span data-ttu-id="0af66-112">Padrões variados</span><span class="sxs-lookup"><span data-stu-id="0af66-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0af66-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0af66-113">Remarks</span></span>

<span data-ttu-id="0af66-114">Para definir o padrão de preenchimento, insira um número de 0 a 40, que é um índice em uma coleção de padrões.</span><span class="sxs-lookup"><span data-stu-id="0af66-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="0af66-115">Você pode exibir a coleção de padrões de preenchimento na caixa de diálogo **preenchimento** (na guia **página inicial** , no grupo **forma** , clique em **preenchimento**e, em seguida, clique em **Opções de preenchimento**).</span><span class="sxs-lookup"><span data-stu-id="0af66-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="0af66-116">Para obter uma referência para a célula ShdwPattern pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="0af66-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0af66-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0af66-117">Cell name:</span></span>  <br/> |<span data-ttu-id="0af66-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="0af66-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="0af66-119">Para obter uma referência para a célula ShdwPattern pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0af66-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0af66-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0af66-120">Section index:</span></span>  <br/> |<span data-ttu-id="0af66-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0af66-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0af66-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0af66-122">Row index:</span></span>  <br/> |<span data-ttu-id="0af66-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0af66-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="0af66-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0af66-124">Cell index:</span></span>  <br/> |<span data-ttu-id="0af66-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="0af66-125">**visFillShdwPattern**</span></span> <br/> |
   

