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
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407610"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="75bb1-103">Célula Action (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="75bb1-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="75bb1-104">Contém a fórmula a ser executada quando o usuário escolhe um comando em um menu de atalho ou de ação de marca.</span><span class="sxs-lookup"><span data-stu-id="75bb1-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="75bb1-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="75bb1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="75bb1-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="75bb1-106">Remarks</span></span>

<span data-ttu-id="75bb1-107">Uma célula Action é avaliada somente quando ocorre a ação, não quando a fórmula é inserida.</span><span class="sxs-lookup"><span data-stu-id="75bb1-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="75bb1-108">Para fazer referência à célula Action pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="75bb1-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75bb1-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="75bb1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="75bb1-110">Ações.</span><span class="sxs-lookup"><span data-stu-id="75bb1-110">Actions.</span></span>  <span data-ttu-id="75bb1-111">*nome*  . Ação em que ações.</span><span class="sxs-lookup"><span data-stu-id="75bb1-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="75bb1-112">*nome*  é o nome da linha de ações</span><span class="sxs-lookup"><span data-stu-id="75bb1-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="75bb1-113">Para fazer referência à célula Action pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="75bb1-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75bb1-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="75bb1-114">Section index:</span></span>  <br/> |<span data-ttu-id="75bb1-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="75bb1-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="75bb1-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="75bb1-116">Row index:</span></span>  <br/> |<span data-ttu-id="75bb1-117">**visRowAction**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="75bb1-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="75bb1-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="75bb1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="75bb1-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="75bb1-119">**visActionAction**</span></span> <br/> |
   

