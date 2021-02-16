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
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426860"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="3aa4d-103">Célula Ask (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="3aa4d-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="3aa4d-104">Determina se um usuário é solicitado a inserir os dados da forma quando uma instância é criada ou a forma é duplicada ou copiada.</span><span class="sxs-lookup"><span data-stu-id="3aa4d-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="3aa4d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3aa4d-105">**Value**</span></span>|<span data-ttu-id="3aa4d-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3aa4d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3aa4d-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="3aa4d-107">TRUE</span></span>  <br/> |<span data-ttu-id="3aa4d-108">Solicita ao usuário inserir dados da forma na caixa de diálogo **Definir Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="3aa4d-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="3aa4d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3aa4d-109">FALSE</span></span>  <br/> |<span data-ttu-id="3aa4d-110">Não solicita ao usuário inserir dados.</span><span class="sxs-lookup"><span data-stu-id="3aa4d-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3aa4d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aa4d-111">Remarks</span></span>

<span data-ttu-id="3aa4d-112">O valor desta célula corresponde à caixa de seleção **Perguntar ao Soltar** da caixa de diálogo **Definir Dados da Forma** (Clique com o botão direito do mouse na forma, aponte para **Dados** e clique em **Definir Dados da Forma**).</span><span class="sxs-lookup"><span data-stu-id="3aa4d-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="3aa4d-113">Para fazer referência à célula Ask pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3aa4d-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-114">Cell name:</span></span>  <br/> |<span data-ttu-id="3aa4d-115">Prop. *nome*  . Verifique onde Prop.  *é*  o nome da linha de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="3aa4d-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="3aa4d-116">Para fazer referência à célula Ask pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3aa4d-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-117">Section index:</span></span>  <br/> |<span data-ttu-id="3aa4d-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="3aa4d-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="3aa4d-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-119">Row index:</span></span>  <br/> |<span data-ttu-id="3aa4d-120">**visRowProp**  +   *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="3aa4d-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="3aa4d-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3aa4d-121">Cell index:</span></span>  <br/> |<span data-ttu-id="3aa4d-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="3aa4d-122">**visCustPropsAsk**</span></span> <br/> |
   

