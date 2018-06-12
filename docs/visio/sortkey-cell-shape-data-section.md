---
title: Célula SortKey (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251345
localization_priority: Normal
ms.assetid: 67fa5389-f0b9-a9db-8d19-9b16e256dfa3
description: Avalia uma cadeia de caracteres que influencia a ordem na qual os itens na janela dados da forma são listados.
ms.openlocfilehash: 1dbc093f2cee509531b8148563fbdb1a777a349f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773043"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="dc7ef-103">Célula SortKey (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="dc7ef-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="dc7ef-104">Avalia uma cadeia de caracteres que influencia a ordem na qual os itens na janela **Dados** da forma são listados.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc7ef-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="dc7ef-105">Remarks</span></span>

<span data-ttu-id="dc7ef-106">O cálculo usado para comparar valores de SortKey é específica de localidade e maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="dc7ef-107">Se os valores de SortKey forem iguais, os dados da forma estão listados na ordem de linha.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="dc7ef-108">Dados da forma que possuem sem chave de classificação são listados depois que os dados de forma que contêm uma chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="dc7ef-109">A seguir está um exemplo de como usar chaves de classificação para exibir os dados da forma na janela **Dados da forma** na ordem: número de itens, quantidade, preço.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="dc7ef-110">*Row, Label* e *SortKey* se referir a células na linha de dados de forma.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="dc7ef-111">Nesse caso, as linhas de dados de forma tenham sido chamadas.</span><span class="sxs-lookup"><span data-stu-id="dc7ef-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="dc7ef-112">**Row**</span><span class="sxs-lookup"><span data-stu-id="dc7ef-112">**Row**</span></span>|<span data-ttu-id="dc7ef-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="dc7ef-113">**Label**</span></span>|<span data-ttu-id="dc7ef-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="dc7ef-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="dc7ef-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="dc7ef-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="dc7ef-116">Número de itens</span><span class="sxs-lookup"><span data-stu-id="dc7ef-116">Item Number</span></span>  <br/> | <span data-ttu-id="dc7ef-117">1</span><span class="sxs-lookup"><span data-stu-id="dc7ef-117">1</span></span>  <br/> |
| <span data-ttu-id="dc7ef-118">Prop</span><span class="sxs-lookup"><span data-stu-id="dc7ef-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="dc7ef-119">Preço</span><span class="sxs-lookup"><span data-stu-id="dc7ef-119">Price</span></span>  <br/> | <span data-ttu-id="dc7ef-120">3</span><span class="sxs-lookup"><span data-stu-id="dc7ef-120">3</span></span>  <br/> |
| <span data-ttu-id="dc7ef-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="dc7ef-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="dc7ef-122">Quantidade</span><span class="sxs-lookup"><span data-stu-id="dc7ef-122">Quantity</span></span>  <br/> | <span data-ttu-id="dc7ef-123">2</span><span class="sxs-lookup"><span data-stu-id="dc7ef-123">2</span></span>  <br/> |
   
<span data-ttu-id="dc7ef-124">Para obter uma referência para a célula SortKey pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc7ef-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-125">Cell name:</span></span>  <br/> | <span data-ttu-id="dc7ef-126">Prop.  *Nome* . SortKey onde Prop.  *Nome* é o nome da linha de propriedade personalizada</span><span class="sxs-lookup"><span data-stu-id="dc7ef-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="dc7ef-127">Para obter uma referência para a célula SortKey pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dc7ef-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-128">Section index:</span></span>  <br/> |<span data-ttu-id="dc7ef-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="dc7ef-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="dc7ef-130">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-130">Row index:</span></span>  <br/> |<span data-ttu-id="dc7ef-131">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dc7ef-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dc7ef-132">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="dc7ef-132">Cell index:</span></span>  <br/> |<span data-ttu-id="dc7ef-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="dc7ef-133">**visCustPropsSortKey**</span></span> <br/> |
   

