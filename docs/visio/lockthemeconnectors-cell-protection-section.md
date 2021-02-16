---
title: Célula LockThemeConnectors (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha Theme Properties seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438404"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="fd497-104">Célula LockThemeConnectors (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="fd497-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="fd497-105">Impede que a **célula ConnectorsSchemeIndex** na linha **Theme Properties** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="fd497-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="fd497-106">Não impede que os usuários editem manualmente esse valor no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd497-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="fd497-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd497-107">**Value**</span></span>|<span data-ttu-id="fd497-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd497-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd497-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="fd497-109">TRUE</span></span>  <br/> |<span data-ttu-id="fd497-110">A **célula ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="fd497-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="fd497-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd497-111">FALSE</span></span>  <br/> |<span data-ttu-id="fd497-112">A **célula ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd497-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd497-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd497-113">Remarks</span></span>

<span data-ttu-id="fd497-114">Para fazer referência à célula **LockThemeConnectors** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="fd497-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd497-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fd497-115">Cell name:</span></span>  <br/> | <span data-ttu-id="fd497-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="fd497-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="fd497-117">Para fazer referência à célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fd497-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd497-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fd497-118">Section index:</span></span>  <br/> |<span data-ttu-id="fd497-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd497-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fd497-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fd497-120">Row index:</span></span>  <br/> |<span data-ttu-id="fd497-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fd497-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="fd497-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="fd497-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fd497-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="fd497-123">**visLockThemeConnectors**</span></span> <br/> |
   

