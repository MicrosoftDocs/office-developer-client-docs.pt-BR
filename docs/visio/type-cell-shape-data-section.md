---
title: Célula Type (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Especifica um tipo de dados para o valor dados da forma.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350894"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="69d86-103">Célula Type (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="69d86-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="69d86-104">Especifica um tipo de dados para o valor dados da forma.</span><span class="sxs-lookup"><span data-stu-id="69d86-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="69d86-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="69d86-105">**Value**</span></span>|<span data-ttu-id="69d86-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="69d86-106">**Description**</span></span>|<span data-ttu-id="69d86-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="69d86-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69d86-108">,0</span><span class="sxs-lookup"><span data-stu-id="69d86-108">0</span></span>  <br/> |<span data-ttu-id="69d86-p101">Sequência de caracteres (padrão).</span><span class="sxs-lookup"><span data-stu-id="69d86-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="69d86-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="69d86-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="69d86-112">1</span><span class="sxs-lookup"><span data-stu-id="69d86-112">1</span></span>  <br/> |<span data-ttu-id="69d86-p102">Lista fixa. Exibe os itens da lista em uma caixa de combinação suspensa na caixa de diálogo **Definir Dados da Forma**. Especifique os itens da lista na célula Format. Os usuários podem selecionar somente um item da lista.</span><span class="sxs-lookup"><span data-stu-id="69d86-p102">Fixed list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select only one item from the list.  </span></span><br/> |<span data-ttu-id="69d86-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="69d86-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="69d86-118">duas</span><span class="sxs-lookup"><span data-stu-id="69d86-118">2</span></span>  <br/> |<span data-ttu-id="69d86-p103">Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="69d86-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="69d86-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="69d86-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="69d86-123">3D</span><span class="sxs-lookup"><span data-stu-id="69d86-123">3</span></span>  <br/> |<span data-ttu-id="69d86-p104">Booliano. Exibe FALSE e TRUE como itens que podem ser selecionados pelo usuário na caixa de lista suspensa da caixa de diálogo **Definir Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="69d86-p104">Boolean. Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.  </span></span><br/> |<span data-ttu-id="69d86-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="69d86-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="69d86-127">quatro</span><span class="sxs-lookup"><span data-stu-id="69d86-127">4</span></span>  <br/> |<span data-ttu-id="69d86-p105">Lista variável. Exibe os itens da lista em uma caixa de combinação suspensa na caixa de diálogo **Definir Dados da Forma**. Especifique os itens da lista na célula Format. Os usuários podem selecionar um item da lista ou inserir um novo item adicionado à lista atual na célula Format.</span><span class="sxs-lookup"><span data-stu-id="69d86-p105">Variable list. Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box. Specify the list items in the Format cell. Users can select a list item or enter a new item that is added to the current list in the Format cell.  </span></span><br/> |<span data-ttu-id="69d86-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="69d86-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="69d86-133">0,5</span><span class="sxs-lookup"><span data-stu-id="69d86-133">5</span></span>  <br/> |<span data-ttu-id="69d86-p106">Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="69d86-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="69d86-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="69d86-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="69d86-138">6</span><span class="sxs-lookup"><span data-stu-id="69d86-138">6</span></span>  <br/> |<span data-ttu-id="69d86-p107">Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="69d86-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="69d86-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="69d86-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="69d86-143">178</span><span class="sxs-lookup"><span data-stu-id="69d86-143">7</span></span>  <br/> |<span data-ttu-id="69d86-p108">Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="69d86-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="69d86-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="69d86-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69d86-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="69d86-148">Remarks</span></span>

<span data-ttu-id="69d86-149">Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="69d86-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69d86-150">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="69d86-150">Cell name:</span></span>  <br/> |<span data-ttu-id="69d86-151">Hélice. *Nome* . Digite onde prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="69d86-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="69d86-152">Para obter uma referência para a célula Type pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="69d86-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69d86-153">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="69d86-153">Section index:</span></span>  <br/> |<span data-ttu-id="69d86-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="69d86-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="69d86-155">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="69d86-155">Row index:</span></span>  <br/> |<span data-ttu-id="69d86-156">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="69d86-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="69d86-157">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="69d86-157">Cell index:</span></span>  <br/> |<span data-ttu-id="69d86-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="69d86-158">**visCustPropsType**</span></span> <br/> |
   

