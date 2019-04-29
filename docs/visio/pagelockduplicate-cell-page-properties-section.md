---
title: Célula PageLockDuplicate (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina se a página pode ser duplicada, como um Boolean.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425978"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="cf88c-103">Célula PageLockDuplicate (seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="cf88c-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="cf88c-104">Determina se a página pode ser duplicada, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="cf88c-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf88c-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf88c-105">TRUE</span></span>  <br/> |<span data-ttu-id="cf88c-106">**Duplicata** no menu de atalho da página e o método de automação **Page. Duplicate** estão desabilitados para a página.</span><span class="sxs-lookup"><span data-stu-id="cf88c-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="cf88c-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf88c-107">FALSE</span></span>  <br/> |<span data-ttu-id="cf88c-108">A página pode ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="cf88c-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf88c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf88c-109">Remarks</span></span>

<span data-ttu-id="cf88c-110">Para obter uma referência para a célula **PageLockDuplicate** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="cf88c-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf88c-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cf88c-111">Cell name:</span></span>  <br/> | <span data-ttu-id="cf88c-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="cf88c-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="cf88c-113">Para obter uma referência para a célula **PageLockDuplicate** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cf88c-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf88c-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cf88c-114">Section index:</span></span>  <br/> |<span data-ttu-id="cf88c-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf88c-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cf88c-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cf88c-116">Row index:</span></span>  <br/> |<span data-ttu-id="cf88c-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="cf88c-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="cf88c-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="cf88c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="cf88c-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="cf88c-119">**visPageLockDuplicate**</span></span> <br/> |
   

