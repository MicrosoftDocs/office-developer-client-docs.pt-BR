---
title: Célula Menu (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772418"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="d848e-103">Célula Menu (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="d848e-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="d848e-104">Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="d848e-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d848e-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="d848e-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d848e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d848e-106">Remarks</span></span>

<span data-ttu-id="d848e-p101">Para inserir um separador no menu acima desse item, use a célula BeginGroup. Para exibir o comando na parte inferior do menu, insira antes do nome o caractere de porcentagem (%) .</span><span class="sxs-lookup"><span data-stu-id="d848e-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="d848e-109">Para obter uma referência para a célula Menu pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d848e-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d848e-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d848e-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d848e-111">Ações.</span><span class="sxs-lookup"><span data-stu-id="d848e-111">Actions.</span></span> <span data-ttu-id="d848e-112">*nome* . Ações de Menuwhere.</span><span class="sxs-lookup"><span data-stu-id="d848e-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="d848e-113">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="d848e-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="d848e-114">Para obter uma referência para a célula Menu pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d848e-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d848e-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d848e-115">Section index:</span></span>  <br/> |<span data-ttu-id="d848e-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="d848e-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="d848e-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d848e-117">Row index:</span></span>  <br/> |<span data-ttu-id="d848e-118">**visRowAction** +  *i* onde i = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="d848e-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="d848e-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d848e-119">Cell index:</span></span>  <br/> |<span data-ttu-id="d848e-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="d848e-120">**visActionMenu**</span></span> <br/> |
   

