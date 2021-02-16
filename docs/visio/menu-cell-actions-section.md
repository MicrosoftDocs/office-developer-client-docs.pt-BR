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
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436325"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="ecc4a-103">Célula Menu (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="ecc4a-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="ecc4a-104">Define o nome de um item de menu exibido em um menu de atalho ou de marca de ação para uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="ecc4a-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ecc4a-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="ecc4a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ecc4a-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecc4a-106">Remarks</span></span>

<span data-ttu-id="ecc4a-p101">Para inserir um separador no menu acima desse item, use a célula BeginGroup. Para exibir o comando na parte inferior do menu, insira antes do nome o caractere de porcentagem (%) .</span><span class="sxs-lookup"><span data-stu-id="ecc4a-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="ecc4a-109">Para fazer referência à célula Menu pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecc4a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="ecc4a-111">Ações.</span><span class="sxs-lookup"><span data-stu-id="ecc4a-111">Actions.</span></span> <span data-ttu-id="ecc4a-112">*nome*  . Menuonde Ações.</span><span class="sxs-lookup"><span data-stu-id="ecc4a-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="ecc4a-113">*nome*  é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="ecc4a-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="ecc4a-114">Para obter uma referência para a célula Menu pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecc4a-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-115">Section index:</span></span>  <br/> |<span data-ttu-id="ecc4a-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="ecc4a-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="ecc4a-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-117">Row index:</span></span>  <br/> |<span data-ttu-id="ecc4a-118">**visRowAction**  +   *i* onde i = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="ecc4a-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="ecc4a-119">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="ecc4a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ecc4a-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="ecc4a-120">**visActionMenu**</span></span> <br/> |
   

