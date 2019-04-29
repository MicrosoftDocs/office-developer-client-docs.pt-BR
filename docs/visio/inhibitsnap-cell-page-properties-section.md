---
title: Célula InhibitSnap (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426748"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="e1556-103">Célula InhibitSnap (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="e1556-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="e1556-104">Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="e1556-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="e1556-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e1556-105">**Value**</span></span>|<span data-ttu-id="e1556-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e1556-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e1556-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="e1556-107">TRUE</span></span>  <br/> | <span data-ttu-id="e1556-108">Inibe qualquer ajuste na página, com exceção da régua e da grade.</span><span class="sxs-lookup"><span data-stu-id="e1556-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="e1556-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e1556-109">FALSE</span></span>  <br/> | <span data-ttu-id="e1556-110">Permite ajustar.</span><span class="sxs-lookup"><span data-stu-id="e1556-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1556-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1556-111">Remarks</span></span>

<span data-ttu-id="e1556-112">Para fazer referência à célula InhibitSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e1556-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1556-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e1556-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e1556-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="e1556-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="e1556-115">Para fazer referência à célula InhibitSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e1556-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1556-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e1556-116">Section index:</span></span>  <br/> |<span data-ttu-id="e1556-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e1556-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e1556-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="e1556-118">Row index:</span></span>  <br/> |<span data-ttu-id="e1556-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="e1556-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="e1556-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="e1556-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e1556-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="e1556-121">**visPageInhibitSnap**</span></span> <br/> |
   

