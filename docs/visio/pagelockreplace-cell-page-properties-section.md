---
title: Célula PageLockReplace (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão Substituir Forma deve ser desabilitado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433098"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="05229-103">Célula PageLockReplace (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="05229-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="05229-104">Indica se o botão **Substituir Forma** deve ser desabilitado para esta página.</span><span class="sxs-lookup"><span data-stu-id="05229-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="05229-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="05229-105">**Value**</span></span>|<span data-ttu-id="05229-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="05229-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05229-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="05229-107">TRUE</span></span>  <br/> |<span data-ttu-id="05229-108">O **botão Alterar** Forma fica es cinza quando esta página está ativa.</span><span class="sxs-lookup"><span data-stu-id="05229-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="05229-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="05229-109">FALSE</span></span>  <br/> |<span data-ttu-id="05229-110">O **botão Alterar** Forma não está desabilitado por esta página.</span><span class="sxs-lookup"><span data-stu-id="05229-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="05229-111">O botão ainda poderá ficar es cinza se: **o DocLockReplace** na **Planilha de Documentos** estiver definido como **VERDADEIRO**; a **célula LockReplace** para a forma selecionada é definida como **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="05229-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05229-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="05229-112">Remarks</span></span>

<span data-ttu-id="05229-113">Para fazer referência à célula **PageLockReplace** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="05229-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05229-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="05229-114">Cell name:</span></span>  <br/> | <span data-ttu-id="05229-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="05229-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="05229-116">Para fazer referência à célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="05229-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="05229-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="05229-117">Section index:</span></span>  <br/> |<span data-ttu-id="05229-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05229-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="05229-119">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="05229-119">Row index:</span></span>  <br/> |<span data-ttu-id="05229-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="05229-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="05229-121">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="05229-121">Cell index:</span></span>  <br/> |<span data-ttu-id="05229-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="05229-122">**visPageLockReplace**</span></span> <br/> |
   

