---
title: Célula Format (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251340
localization_priority: Normal
ms.assetid: c36fc895-5577-59f6-0ff5-5892ca81a58f
description: Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.
ms.openlocfilehash: bb02cfefd6dc93798ca5e2b0c657e4616515fd0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415359"
---
# <a name="format-cell-shape-data-section"></a><span data-ttu-id="56853-103">Célula Format (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="56853-103">Format Cell (Shape Data Section)</span></span>

<span data-ttu-id="56853-104">Especifica a formatação de um item de dados da forma que pode ser uma sequência de caracteres, uma lista fixa, um número, uma lista variável, uma data ou hora, uma duração ou uma moeda.</span><span class="sxs-lookup"><span data-stu-id="56853-104">Specifies the formatting of a shape data item that is a string, a fixed list, a number, a variable list, a date or time, a duration, or a currency.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56853-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="56853-105">Remarks</span></span>

|<span data-ttu-id="56853-106">**Tipo de item de dados da forma**</span><span class="sxs-lookup"><span data-stu-id="56853-106">**Shape data item type**</span></span>|<span data-ttu-id="56853-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="56853-107">**Value**</span></span>|<span data-ttu-id="56853-108">**Conteúdo da célula Format**</span><span class="sxs-lookup"><span data-stu-id="56853-108">**Format cell contents**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="56853-109">String</span><span class="sxs-lookup"><span data-stu-id="56853-109">String</span></span>  <br/> | <span data-ttu-id="56853-110">0</span><span class="sxs-lookup"><span data-stu-id="56853-110">0</span></span>  <br/> | <span data-ttu-id="56853-111">Uma figura de formatação apropriada para o tipo de dado.</span><span class="sxs-lookup"><span data-stu-id="56853-111">A format picture appropriate for the data type.</span></span>  <br/> |
| <span data-ttu-id="56853-112">Lista fixa</span><span class="sxs-lookup"><span data-stu-id="56853-112">Fixed list</span></span>  <br/> | <span data-ttu-id="56853-113">1 </span><span class="sxs-lookup"><span data-stu-id="56853-113">1</span></span>  <br/> | <span data-ttu-id="56853-114">Os itens a serem exibidos na lista, separados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="56853-114">The items to appear in the list, separated by semicolons.</span></span>  <br/> |
| <span data-ttu-id="56853-115">Número</span><span class="sxs-lookup"><span data-stu-id="56853-115">Number</span></span>  <br/> | <span data-ttu-id="56853-116">2 </span><span class="sxs-lookup"><span data-stu-id="56853-116">2</span></span>  <br/> | <span data-ttu-id="56853-117">Uma figura de formatação apropriada para o tipo de dado.</span><span class="sxs-lookup"><span data-stu-id="56853-117">A format picture appropriate for the data type.</span></span>  <br/> |
| <span data-ttu-id="56853-118">Lista variável</span><span class="sxs-lookup"><span data-stu-id="56853-118">Variable list</span></span>  <br/> | <span data-ttu-id="56853-119">4 </span><span class="sxs-lookup"><span data-stu-id="56853-119">4</span></span>  <br/> | <span data-ttu-id="56853-120">Os itens a serem exibidos na lista, separados por ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="56853-120">The items to appear in the list, separated by semicolons.</span></span>  <br/> |
| <span data-ttu-id="56853-121">Data ou hora</span><span class="sxs-lookup"><span data-stu-id="56853-121">Date or time</span></span>  <br/> | <span data-ttu-id="56853-122">5 </span><span class="sxs-lookup"><span data-stu-id="56853-122">5</span></span>  <br/> | <span data-ttu-id="56853-123">Uma figura de formatação apropriada para o tipo de dado.</span><span class="sxs-lookup"><span data-stu-id="56853-123">A format picture appropriate for the data type.</span></span>  <br/> |
| <span data-ttu-id="56853-124">Duration</span><span class="sxs-lookup"><span data-stu-id="56853-124">Duration</span></span>  <br/> | <span data-ttu-id="56853-125">6 </span><span class="sxs-lookup"><span data-stu-id="56853-125">6</span></span>  <br/> | <span data-ttu-id="56853-126">Uma figura de formatação apropriada para o tipo de dado.</span><span class="sxs-lookup"><span data-stu-id="56853-126">A format picture appropriate for the data type.</span></span>  <br/> |
| <span data-ttu-id="56853-127">Moeda</span><span class="sxs-lookup"><span data-stu-id="56853-127">Currency</span></span>  <br/> | <span data-ttu-id="56853-128">7 </span><span class="sxs-lookup"><span data-stu-id="56853-128">7</span></span>  <br/> | <span data-ttu-id="56853-129">Uma figura de formatação apropriada para o tipo de dado.</span><span class="sxs-lookup"><span data-stu-id="56853-129">A format picture appropriate for the data type.</span></span>  <br/> |
   
<span data-ttu-id="56853-p101">Um exemplo de especificação de uma figura de formatação apropriada para o tipo de dado é a figura de formatação "# #/4 UU" que formata o número 12,43 pol. como 12 2/4 POLEGADAS. Para obter mais informações sobre como especificar uma figura de formatação, consulte [Sobre figuras de formatação](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="56853-p101">As an example of specifying a format picture appropriate for the data type, the format picture "# #/4 UU" formats the number 12.43 in. as 12 2/4 INCHES. For more information about specifying a format picture, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="56853-133">Um exemplo de itens de especificação de uma lista é "Engenharia;Recursos humanos;Vendas;Marketing".</span><span class="sxs-lookup"><span data-stu-id="56853-133">An example of specifying items for a list is "Engineering;Human Resources;Sales;Marketing".</span></span>
  
<span data-ttu-id="56853-p102">Os valores de data (tipo = 5) são exibidos no formato de data abreviada. Os valores de moeda (tipo = 7) são exibidos usando a configuração atual do usuário para **Moeda** na guia **Opções Regionais** no item **Opções Regionais e de Idioma** do **Painel de Controle**.</span><span class="sxs-lookup"><span data-stu-id="56853-p102">Date values (type = 5) are displayed in the short date format. Currency values (type = 7) are displayed using the user's current setting for **Currency** on the **Regional Options** tab in the **Regional and Language Options** item in **Control Panel**.</span></span>
  
<span data-ttu-id="56853-p103">Um número (tipo = 2) pode representar uma dimensão, uma grandeza escalar, um ângulo, uma data, uma hora ou uma moeda. Para garantir que um número de entrada seja sempre avaliado como uma data, hora ou moeda, utilize as funções DATETIME ou CY na célula Format em vez de uma figura de formatação.</span><span class="sxs-lookup"><span data-stu-id="56853-p103">A number (type = 2) can represent a dimension, scalar, angle, date, time, or currency. To ensure that an input number is always evaluated as a date, time, or currency, use the DATETIME or CY function in the Format cell instead of a format picture.</span></span>
  
<span data-ttu-id="56853-138">Para fazer referência à célula Format pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="56853-138">To get a reference to the Format cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56853-139">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="56853-139">Cell name:</span></span>  <br/> | <span data-ttu-id="56853-140">Prop.  *nome*  . Formatar onde Prop.  *nome*  é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="56853-140">Prop.  *name*  .Format            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="56853-141">Para fazer referência à célula Format pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="56853-141">To get a reference to the Format cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56853-142">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="56853-142">Section index:</span></span>  <br/> |<span data-ttu-id="56853-143">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="56853-143">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="56853-144">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="56853-144">Row index:</span></span>  <br/> |<span data-ttu-id="56853-145">**visRowProp**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56853-145">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56853-146">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="56853-146">Cell index:</span></span>  <br/> |<span data-ttu-id="56853-147">**visCustPropsFormat**</span><span class="sxs-lookup"><span data-stu-id="56853-147">**visCustPropsFormat**</span></span> <br/> |
   

