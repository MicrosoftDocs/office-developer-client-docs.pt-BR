---
title: Célula Action (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771242"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="948f0-103">Célula Action (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="948f0-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="948f0-104">Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.</span><span class="sxs-lookup"><span data-stu-id="948f0-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="948f0-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="948f0-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="948f0-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="948f0-106">Remarks</span></span>

<span data-ttu-id="948f0-107">Uma célula Action é avaliada somente quando ocorre a ação, não quando a fórmula é inserida.</span><span class="sxs-lookup"><span data-stu-id="948f0-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="948f0-108">Para fazer referência à célula Action pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="948f0-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="948f0-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="948f0-109">Cell name:</span></span>  <br/> | <span data-ttu-id="948f0-110">Ações.</span><span class="sxs-lookup"><span data-stu-id="948f0-110">Actions.</span></span>  <span data-ttu-id="948f0-111">*nome* . Ação onde ações.</span><span class="sxs-lookup"><span data-stu-id="948f0-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="948f0-112">*nome* é o nome da linha actions</span><span class="sxs-lookup"><span data-stu-id="948f0-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="948f0-113">Para fazer referência à célula Action pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="948f0-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="948f0-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="948f0-114">Section index:</span></span>  <br/> |<span data-ttu-id="948f0-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="948f0-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="948f0-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="948f0-116">Row index:</span></span>  <br/> |<span data-ttu-id="948f0-117">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="948f0-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="948f0-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="948f0-118">Cell index:</span></span>  <br/> |<span data-ttu-id="948f0-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="948f0-119">**visActionAction**</span></span> <br/> |
   

