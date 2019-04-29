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
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422520"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="97b0c-103">Célula LockCustProp (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="97b0c-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="97b0c-104">Estabelece se o usuário pode adicionar, excluir ou modificar dados da forma na interface do usuário (UI) usando a caixa de diálogo **Definir Dados da Forma** ou o menu de atalho para a janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="97b0c-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="97b0c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="97b0c-105">**Value**</span></span>|<span data-ttu-id="97b0c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="97b0c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97b0c-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="97b0c-107">TRUE</span></span>  <br/> |<span data-ttu-id="97b0c-108">O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é desabilitado.</span><span class="sxs-lookup"><span data-stu-id="97b0c-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="97b0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="97b0c-109">FALSE</span></span>  <br/> |<span data-ttu-id="97b0c-110">O comando **Definir Dados da Forma** no menu de atalho da janela **Dados da Forma** é habilitado (padrão).</span><span class="sxs-lookup"><span data-stu-id="97b0c-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b0c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="97b0c-111">Remarks</span></span>

<span data-ttu-id="97b0c-112">Um valor VERDADEIRO não evita que um usuário altere o valor de um item de dados da forma ou altere a seção Shape Data na janela ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="97b0c-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="97b0c-113">Para obter uma referência para a célula LockCustProp pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="97b0c-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b0c-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="97b0c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="97b0c-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="97b0c-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="97b0c-116">Para obter uma referência para a célula LockCustProp pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="97b0c-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b0c-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="97b0c-117">Section index:</span></span>  <br/> |<span data-ttu-id="97b0c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97b0c-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="97b0c-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="97b0c-119">Row index:</span></span>  <br/> |<span data-ttu-id="97b0c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="97b0c-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="97b0c-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="97b0c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="97b0c-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="97b0c-122">**visLockCustProp**</span></span> <br/> |
   

