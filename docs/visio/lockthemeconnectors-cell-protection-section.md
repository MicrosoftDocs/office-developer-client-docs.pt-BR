---
title: Célula LockThemeConnectors (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha de propriedades do tema seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348234"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="6b929-104">Célula LockThemeConnectors (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="6b929-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="6b929-105">Impede que a célula **ConnectorsSchemeIndex** na linha de **Propriedades do tema** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="6b929-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="6b929-106">Não impede que os usuários editem manualmente esse valor no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6b929-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="6b929-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6b929-107">**Value**</span></span>|<span data-ttu-id="6b929-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b929-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b929-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b929-109">TRUE</span></span>  <br/> |<span data-ttu-id="6b929-110">A célula **ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6b929-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="6b929-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6b929-111">FALSE</span></span>  <br/> |<span data-ttu-id="6b929-112">A célula **ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b929-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b929-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b929-113">Remarks</span></span>

<span data-ttu-id="6b929-114">Para obter uma referência para a célula **LockThemeConnectors** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="6b929-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b929-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6b929-115">Cell name:</span></span>  <br/> | <span data-ttu-id="6b929-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="6b929-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="6b929-117">Para obter uma referência para a célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6b929-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b929-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6b929-118">Section index:</span></span>  <br/> |<span data-ttu-id="6b929-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b929-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b929-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6b929-120">Row index:</span></span>  <br/> |<span data-ttu-id="6b929-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6b929-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6b929-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6b929-122">Cell index:</span></span>  <br/> |<span data-ttu-id="6b929-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="6b929-123">**visLockThemeConnectors**</span></span> <br/> |
   

