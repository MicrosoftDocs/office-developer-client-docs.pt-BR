---
title: Célula LockCustProp (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo Definir Dados da Forma ou o menu de atalho para a janela Dados da Forma.
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772244"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="37515-103">Célula LockCustProp (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="37515-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="37515-104">Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo **Definir Dados da Forma** ou o menu de atalho para a janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="37515-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="37515-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="37515-105">**Value**</span></span>|<span data-ttu-id="37515-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="37515-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37515-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="37515-107">TRUE</span></span>  <br/> |<span data-ttu-id="37515-108">
          O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é desabilitado.
</span><span class="sxs-lookup"><span data-stu-id="37515-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="37515-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="37515-109">FALSE</span></span>  <br/> |<span data-ttu-id="37515-110">
          O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é habilitado (padrão).
</span><span class="sxs-lookup"><span data-stu-id="37515-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37515-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="37515-111">Remarks</span></span>

<span data-ttu-id="37515-112">Um valor VERDADEIRO não evita que um usuário altere o valor de um item de dados da forma ou altere a seção Shape Data na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="37515-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="37515-113">Para obter uma referência para a célula LockCustProp pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="37515-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37515-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="37515-114">Cell name:</span></span>  <br/> |<span data-ttu-id="37515-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="37515-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="37515-116">Para obter uma referência para a célula LockCustProp pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="37515-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37515-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="37515-117">Section index:</span></span>  <br/> |<span data-ttu-id="37515-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="37515-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37515-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="37515-119">Row index:</span></span>  <br/> |<span data-ttu-id="37515-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="37515-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="37515-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="37515-121">Cell index:</span></span>  <br/> |<span data-ttu-id="37515-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="37515-122">**visLockCustProp**</span></span> <br/> |
   

