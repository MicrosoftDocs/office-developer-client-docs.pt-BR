---
title: Célula LockThemeConnectors (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impede que a célula ConnectorsSchemeIndex na linha de propriedades do tema que está sendo alterado a aplicação de um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772270"
---
# <a name="lockthemeconnectors-cell-protection-section"></a><span data-ttu-id="01428-104">Célula LockThemeConnectors (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="01428-104">LockThemeConnectors Cell (Protection Section)</span></span>

<span data-ttu-id="01428-105">Impede que a célula **ConnectorsSchemeIndex** na linha de **Propriedades do tema** que está sendo alterado a aplicação de um novo tema ou selecionando um novo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="01428-105">Prevents the **ConnectorsSchemeIndex** cell in the **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="01428-106">Não impede que usuários editando manualmente esse valor na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="01428-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="01428-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="01428-107">**Value**</span></span>|<span data-ttu-id="01428-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="01428-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01428-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="01428-109">TRUE</span></span>  <br/> |<span data-ttu-id="01428-110">A célula **ConnectorsSchemeIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.</span><span class="sxs-lookup"><span data-stu-id="01428-110">The **ConnectorsSchemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="01428-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="01428-111">FALSE</span></span>  <br/> |<span data-ttu-id="01428-112">A célula **ConnectorsSchemeIndex** pode ser alterada de seu valor atual por meio da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="01428-112">The **ConnectorsSchemeIndex** cell can be changed from its current value through the UI.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01428-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="01428-113">Remarks</span></span>

<span data-ttu-id="01428-114">Para fazer referência à célula **LockThemeConnectors** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="01428-114">To get a reference to the **LockThemeConnectors** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01428-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="01428-115">Cell name:</span></span>  <br/> | <span data-ttu-id="01428-116">LockThemeConnectors</span><span class="sxs-lookup"><span data-stu-id="01428-116">LockThemeConnectors</span></span>  <br/> |
   
<span data-ttu-id="01428-117">Para obter uma referência à célula **LockThemeConnectors** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="01428-117">To get a reference to the **LockThemeConnectors** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="01428-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="01428-118">Section index:</span></span>  <br/> |<span data-ttu-id="01428-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="01428-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="01428-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="01428-120">Row index:</span></span>  <br/> |<span data-ttu-id="01428-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="01428-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="01428-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="01428-122">Cell index:</span></span>  <br/> |<span data-ttu-id="01428-123">**visLockThemeConnectors**</span><span class="sxs-lookup"><span data-stu-id="01428-123">**visLockThemeConnectors**</span></span> <br/> |
   

