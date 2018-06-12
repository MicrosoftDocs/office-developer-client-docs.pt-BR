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
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772077"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="5d70c-103">Célula InhibitSnap (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="5d70c-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="5d70c-104">Determina se as formas em uma página de primeiro plano são ajustadas a outros objetos na página e a outras formas na página de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="5d70c-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="5d70c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5d70c-105">**Value**</span></span>|<span data-ttu-id="5d70c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5d70c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5d70c-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="5d70c-107">TRUE</span></span>  <br/> | <span data-ttu-id="5d70c-108">Inibe qualquer ajuste na página, com exceção da régua e da grade.</span><span class="sxs-lookup"><span data-stu-id="5d70c-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="5d70c-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="5d70c-109">FALSE</span></span>  <br/> | <span data-ttu-id="5d70c-110">Permite ajustar.</span><span class="sxs-lookup"><span data-stu-id="5d70c-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d70c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d70c-111">Remarks</span></span>

<span data-ttu-id="5d70c-112">Para obter uma referência à célula InhibitSnap pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="5d70c-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d70c-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5d70c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5d70c-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="5d70c-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="5d70c-115">Para obter uma referência à célula InhibitSnap pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5d70c-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5d70c-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5d70c-116">Section index:</span></span>  <br/> |<span data-ttu-id="5d70c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5d70c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5d70c-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5d70c-118">Row index:</span></span>  <br/> |<span data-ttu-id="5d70c-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5d70c-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5d70c-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5d70c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5d70c-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="5d70c-121">**visPageInhibitSnap**</span></span> <br/> |
   

