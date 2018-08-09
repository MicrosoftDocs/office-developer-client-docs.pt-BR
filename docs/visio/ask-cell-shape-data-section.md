---
title: Célula Ask (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Determina se um usuário é solicitado a inserir os dados da forma quando uma instância é criada ou a forma é duplicada ou copiada.
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771262"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="60f29-103">Célula Ask (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="60f29-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="60f29-104">Determina se um usuário é solicitado a inserir os dados da forma quando uma instância é criada ou a forma é duplicada ou copiada.</span><span class="sxs-lookup"><span data-stu-id="60f29-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="60f29-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60f29-105">**Value**</span></span>|<span data-ttu-id="60f29-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="60f29-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60f29-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="60f29-107">TRUE</span></span>  <br/> |<span data-ttu-id="60f29-108">
          Solicita ao usuário inserir dados da forma na caixa de diálogo **Definir Dados da Forma**.
</span><span class="sxs-lookup"><span data-stu-id="60f29-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="60f29-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="60f29-109">FALSE</span></span>  <br/> |<span data-ttu-id="60f29-110">
          Não solicita ao usuário inserir dados.
</span><span class="sxs-lookup"><span data-stu-id="60f29-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60f29-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60f29-111">Remarks</span></span>

<span data-ttu-id="60f29-112">O valor desta célula corresponde à caixa de seleção **Perguntar ao Soltar** da caixa de diálogo **Definir Dados da Forma** (Clique com o botão direito do mouse na forma, aponte para **Dados** e clique em **Definir Dados da Forma**).</span><span class="sxs-lookup"><span data-stu-id="60f29-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="60f29-113">Para fazer referência à célula Ask pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="60f29-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60f29-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="60f29-114">Cell name:</span></span>  <br/> |<span data-ttu-id="60f29-115">Prop. *nome* . Verificar onde Prop.  *nome* é o nome da linha de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="60f29-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="60f29-116">Para fazer referência à célula Ask pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="60f29-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60f29-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="60f29-117">Section index:</span></span>  <br/> |<span data-ttu-id="60f29-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="60f29-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="60f29-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="60f29-119">Row index:</span></span>  <br/> |<span data-ttu-id="60f29-120">**visRowProp** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="60f29-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="60f29-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="60f29-121">Cell index:</span></span>  <br/> |<span data-ttu-id="60f29-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="60f29-122">**visCustPropsAsk**</span></span> <br/> |
   

