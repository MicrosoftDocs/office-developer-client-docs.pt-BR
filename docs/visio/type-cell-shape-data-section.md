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
description: Especifica um tipo de dado para o valor de dados da forma.
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773196"
---
# <a name="type-cell-shape-data-section"></a><span data-ttu-id="06cc1-103">Célula Type (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="06cc1-103">Type Cell (Shape Data Section)</span></span>

<span data-ttu-id="06cc1-104">Especifica um tipo de dado para o valor de dados da forma.</span><span class="sxs-lookup"><span data-stu-id="06cc1-104">Specifies a data type for the shape data value.</span></span>
  
|<span data-ttu-id="06cc1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="06cc1-105">**Value**</span></span>|<span data-ttu-id="06cc1-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06cc1-106">**Description**</span></span>|<span data-ttu-id="06cc1-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="06cc1-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="06cc1-108">0</span><span class="sxs-lookup"><span data-stu-id="06cc1-108">0</span></span>  <br/> |<span data-ttu-id="06cc1-p101">Sequência de caracteres (padrão).</span><span class="sxs-lookup"><span data-stu-id="06cc1-p101">String. This is the default.</span></span>  <br/> |<span data-ttu-id="06cc1-111">**visPropTypeString**</span><span class="sxs-lookup"><span data-stu-id="06cc1-111">**visPropTypeString**</span></span> <br/> |
|<span data-ttu-id="06cc1-112">1</span><span class="sxs-lookup"><span data-stu-id="06cc1-112">1</span></span>  <br/> |<span data-ttu-id="06cc1-113">Lista fixa.</span><span class="sxs-lookup"><span data-stu-id="06cc1-113">Fixed list.</span></span> <span data-ttu-id="06cc1-114">Exibe os itens de lista em uma combinação suspensa caixa na caixa de diálogo **Definir dados da forma** .</span><span class="sxs-lookup"><span data-stu-id="06cc1-114">Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="06cc1-115">Especifique os itens da lista na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-115">Specify the list items in the Format cell.</span></span> <span data-ttu-id="06cc1-116">Os usuários podem selecionar somente um item da lista.</span><span class="sxs-lookup"><span data-stu-id="06cc1-116">Users can select only one item from the list.</span></span>  <br/> |<span data-ttu-id="06cc1-117">**visPropTypeListFix**</span><span class="sxs-lookup"><span data-stu-id="06cc1-117">**visPropTypeListFix**</span></span> <br/> |
|<span data-ttu-id="06cc1-118">2</span><span class="sxs-lookup"><span data-stu-id="06cc1-118">2</span></span>  <br/> |<span data-ttu-id="06cc1-p103">Número. Inclui valores de data, hora, duração e moeda, bem como grandezas escalares, dimensões e ângulos. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-p103">Number. Includes date, time, duration, and currency values as well as scalars, dimensions, and angles. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="06cc1-122">**visPropTypeNumber**</span><span class="sxs-lookup"><span data-stu-id="06cc1-122">**visPropTypeNumber**</span></span> <br/> |
|<span data-ttu-id="06cc1-123">3</span><span class="sxs-lookup"><span data-stu-id="06cc1-123">3</span></span>  <br/> |<span data-ttu-id="06cc1-124">Boolean.</span><span class="sxs-lookup"><span data-stu-id="06cc1-124">Boolean.</span></span> <span data-ttu-id="06cc1-125">Exibe Falso e verdadeiro como itens que os usuários podem selecionar de uma caixa de listagem suspensa na caixa de diálogo **Definir dados da forma** .</span><span class="sxs-lookup"><span data-stu-id="06cc1-125">Displays FALSE and TRUE as items users can select from a drop-down list box in the **Define Shape Data** dialog box.</span></span>  <br/> |<span data-ttu-id="06cc1-126">**visPropTypeBool**</span><span class="sxs-lookup"><span data-stu-id="06cc1-126">**visPropTypeBool**</span></span> <br/> |
|<span data-ttu-id="06cc1-127">4</span><span class="sxs-lookup"><span data-stu-id="06cc1-127">4</span></span>  <br/> |<span data-ttu-id="06cc1-128">Lista variável.</span><span class="sxs-lookup"><span data-stu-id="06cc1-128">Variable list.</span></span> <span data-ttu-id="06cc1-129">Exibe os itens de lista em uma combinação suspensa caixa na caixa de diálogo **Definir dados da forma** .</span><span class="sxs-lookup"><span data-stu-id="06cc1-129">Displays the list items in a drop-down combo box in the **Define Shape Data** dialog box.</span></span> <span data-ttu-id="06cc1-130">Especifique os itens da lista na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-130">Specify the list items in the Format cell.</span></span> <span data-ttu-id="06cc1-131">Os usuários podem selecionar um item de lista ou digitar um novo item é adicionado à lista atual na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-131">Users can select a list item or enter a new item that is added to the current list in the Format cell.</span></span>  <br/> |<span data-ttu-id="06cc1-132">**visPropTypeListVar**</span><span class="sxs-lookup"><span data-stu-id="06cc1-132">**visPropTypeListVar**</span></span> <br/> |
|<span data-ttu-id="06cc1-133">5</span><span class="sxs-lookup"><span data-stu-id="06cc1-133">5</span></span>  <br/> |<span data-ttu-id="06cc1-p106">Valor de data ou hora. Exibe dias, meses e anos ou segundos, minutos e horas ou, ainda, um valor combinado de data e hora. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-p106">Date or time value. Displays days, months, and years, or seconds, minutes, and hours, or a combined date and time value. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="06cc1-137">**visPropTypeDate**</span><span class="sxs-lookup"><span data-stu-id="06cc1-137">**visPropTypeDate**</span></span> <br/> |
|<span data-ttu-id="06cc1-138">6</span><span class="sxs-lookup"><span data-stu-id="06cc1-138">6</span></span>  <br/> |<span data-ttu-id="06cc1-p107">Valor de duração. Exibe o tempo decorrido. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-p107">Duration value. Displays elapsed time. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="06cc1-142">**visPropTypeDuration**</span><span class="sxs-lookup"><span data-stu-id="06cc1-142">**visPropTypeDuration**</span></span> <br/> |
|<span data-ttu-id="06cc1-143">7</span><span class="sxs-lookup"><span data-stu-id="06cc1-143">7</span></span>  <br/> |<span data-ttu-id="06cc1-p108">Valor de moeda. Utiliza as configurações regionais de moeda do sistema. Especifique uma figura de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="06cc1-p108">Currency value. Uses the system's current Regional Settings. Specify a format picture in the Format cell.</span></span>  <br/> |<span data-ttu-id="06cc1-147">**visPropTypeCurrency**</span><span class="sxs-lookup"><span data-stu-id="06cc1-147">**visPropTypeCurrency**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06cc1-148">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="06cc1-148">Remarks</span></span>

<span data-ttu-id="06cc1-149">Para obter uma referência à célula Type pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="06cc1-149">To get a reference to the Type cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06cc1-150">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="06cc1-150">Cell name:</span></span>  <br/> |<span data-ttu-id="06cc1-151">Prop. *Nome* . Tipo onde Prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="06cc1-151">Prop. *Name*  .Type where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="06cc1-152">Para obter uma referência à célula Type pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="06cc1-152">To get a reference to the Type cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06cc1-153">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="06cc1-153">Section index:</span></span>  <br/> |<span data-ttu-id="06cc1-154">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="06cc1-154">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="06cc1-155">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="06cc1-155">Row index:</span></span>  <br/> |<span data-ttu-id="06cc1-156">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="06cc1-156">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="06cc1-157">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="06cc1-157">Cell index:</span></span>  <br/> |<span data-ttu-id="06cc1-158">**visCustPropsType**</span><span class="sxs-lookup"><span data-stu-id="06cc1-158">**visCustPropsType**</span></span> <br/> |
   

