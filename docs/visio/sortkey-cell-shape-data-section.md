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
description: Resulta em uma cadeia de caracteres que influencia a ordem na qual os itens na janela Dados da Forma são listados.
ms.openlocfilehash: d166ea18a36f6a4101b8933fce804be2243954bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417851"
---
# <a name="sortkey-cell-shape-data-section"></a><span data-ttu-id="39a8d-103">Célula SortKey (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="39a8d-103">SortKey Cell (Shape Data Section)</span></span>

<span data-ttu-id="39a8d-104">Avalia uma cadeia de caracteres que influencia a ordem em que os itens são listados na janela **Dados de Forma**.</span><span class="sxs-lookup"><span data-stu-id="39a8d-104">Evaluates to a string that influences the order in which items in the **Shape Data** window are listed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="39a8d-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="39a8d-105">Remarks</span></span>

<span data-ttu-id="39a8d-106">O cálculo utilizado para comparar os valores da célula SortKey são específicos à localidade e sem diferenciação de maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39a8d-106">The calculation used to compare SortKey values is locale-specific and case insensitive.</span></span> <span data-ttu-id="39a8d-107">Se os valores de SortKey forem iguais, os dados da forma serão listados em fila.</span><span class="sxs-lookup"><span data-stu-id="39a8d-107">If SortKey values are equal, the shape data is listed in row order.</span></span> <span data-ttu-id="39a8d-108">Os dados da forma que não têm chave de classificação são listados após os dados da forma que contêm uma chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="39a8d-108">Shape data that have no sort key are listed after shape data that contain a sort key.</span></span>
  
<span data-ttu-id="39a8d-109">O exemplo a seguir mostra como utilizar as chaves de classificação para exibir os dados de forma na janela **Dados da Forma** na ordem: Número de Itens, Quantidade, Preço.</span><span class="sxs-lookup"><span data-stu-id="39a8d-109">Following is an example of using sort keys to display the shape data in the **Shape Data** window in the order: Item Number, Quantity, Price.</span></span> 
  
 <span data-ttu-id="39a8d-110">*Row, Label e*  *SortKey*  referem-se às células na linha de dados da forma.</span><span class="sxs-lookup"><span data-stu-id="39a8d-110">*Row, Label,*  and  *SortKey*  refer to cells in the shape data row.</span></span> <span data-ttu-id="39a8d-111">Neste caso, as linhas de dados de forma foram nomeadas.</span><span class="sxs-lookup"><span data-stu-id="39a8d-111">In this case, the shape data rows have been named.</span></span> 
  
|<span data-ttu-id="39a8d-112">**Linha**</span><span class="sxs-lookup"><span data-stu-id="39a8d-112">**Row**</span></span>|<span data-ttu-id="39a8d-113">**Label**</span><span class="sxs-lookup"><span data-stu-id="39a8d-113">**Label**</span></span>|<span data-ttu-id="39a8d-114">**SortKey**</span><span class="sxs-lookup"><span data-stu-id="39a8d-114">**SortKey**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="39a8d-115">Prop.Item</span><span class="sxs-lookup"><span data-stu-id="39a8d-115">Prop.Item</span></span>  <br/> | <span data-ttu-id="39a8d-116">Número de itens</span><span class="sxs-lookup"><span data-stu-id="39a8d-116">Item Number</span></span>  <br/> | <span data-ttu-id="39a8d-117">1 </span><span class="sxs-lookup"><span data-stu-id="39a8d-117">1</span></span>  <br/> |
| <span data-ttu-id="39a8d-118">Prop.Price</span><span class="sxs-lookup"><span data-stu-id="39a8d-118">Prop.Price</span></span>  <br/> | <span data-ttu-id="39a8d-119">Price</span><span class="sxs-lookup"><span data-stu-id="39a8d-119">Price</span></span>  <br/> | <span data-ttu-id="39a8d-120">3 </span><span class="sxs-lookup"><span data-stu-id="39a8d-120">3</span></span>  <br/> |
| <span data-ttu-id="39a8d-121">Prop.Quan</span><span class="sxs-lookup"><span data-stu-id="39a8d-121">Prop.Quan</span></span>  <br/> | <span data-ttu-id="39a8d-122">Quantidade</span><span class="sxs-lookup"><span data-stu-id="39a8d-122">Quantity</span></span>  <br/> | <span data-ttu-id="39a8d-123">2 </span><span class="sxs-lookup"><span data-stu-id="39a8d-123">2</span></span>  <br/> |
   
<span data-ttu-id="39a8d-124">Para obter uma referência para a célula SortKey pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="39a8d-124">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39a8d-125">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="39a8d-125">Cell name:</span></span>  <br/> | <span data-ttu-id="39a8d-126">Prop.  *Nome*  . SortKey onde Prop.  *Nome*  é o nome da linha de propriedade personalizada</span><span class="sxs-lookup"><span data-stu-id="39a8d-126">Prop.  *Name*  .SortKey where Prop.  *Name*  is the name of the custom property row</span></span>  <br/> |
   
<span data-ttu-id="39a8d-127">Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="39a8d-127">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39a8d-128">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="39a8d-128">Section index:</span></span>  <br/> |<span data-ttu-id="39a8d-129">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="39a8d-129">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="39a8d-130">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="39a8d-130">Row index:</span></span>  <br/> |<span data-ttu-id="39a8d-131">**visRowProp**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="39a8d-131">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="39a8d-132">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="39a8d-132">Cell index:</span></span>  <br/> |<span data-ttu-id="39a8d-133">**visCustPropsSortKey**</span><span class="sxs-lookup"><span data-stu-id="39a8d-133">**visCustPropsSortKey**</span></span> <br/> |
   

