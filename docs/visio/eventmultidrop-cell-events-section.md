---
title: Célula EventMultiDrop (Seção Eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771830"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="d275e-102">Célula EventMultiDrop (Seção Eventos)</span><span class="sxs-lookup"><span data-stu-id="d275e-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="d275e-103">Uma célula de evento que é avaliada quando várias formas são colocadas na página de desenho, como instâncias ou quando as formas são duplicar ou colar.</span><span class="sxs-lookup"><span data-stu-id="d275e-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="d275e-104">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="d275e-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="d275e-105">Para fazer referência à célula EventMultiDrop pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d275e-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d275e-106">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d275e-106">Cell name:</span></span>  <br/> |<span data-ttu-id="d275e-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="d275e-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="d275e-108">Para fazer referência à célula EventMultiDrop pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d275e-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d275e-109">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d275e-109">Section index:</span></span>  <br/> |<span data-ttu-id="d275e-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d275e-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d275e-111">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d275e-111">Row index:</span></span>  <br/> |<span data-ttu-id="d275e-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="d275e-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="d275e-113">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d275e-113">Cell index:</span></span>  <br/> |<span data-ttu-id="d275e-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="d275e-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

