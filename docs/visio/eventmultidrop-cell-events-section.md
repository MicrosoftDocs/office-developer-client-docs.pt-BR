---
title: Célula EventMultiDrop (Seção Eventos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416717"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="3f600-102">Célula EventMultiDrop (Seção Eventos)</span><span class="sxs-lookup"><span data-stu-id="3f600-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="3f600-103">Uma célula de evento que é avaliada quando várias formas são retiradas na página de desenho, como instâncias ou quando as formas são duplicadas ou copiadas.</span><span class="sxs-lookup"><span data-stu-id="3f600-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="3f600-104">As células de evento são avaliadas somente quando ocorre o evento, e não ao inserir a fórmula.</span><span class="sxs-lookup"><span data-stu-id="3f600-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="3f600-105">Para referir-se à célula EventMultiDrop pelo nome de outra fórmula ou a partir de um programa usando a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="3f600-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f600-106">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3f600-106">Cell name:</span></span>  <br/> |<span data-ttu-id="3f600-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="3f600-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="3f600-108">Para referir-se à célula EventMultiDrop pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3f600-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f600-109">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3f600-109">Section index:</span></span>  <br/> |<span data-ttu-id="3f600-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f600-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3f600-111">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3f600-111">Row index:</span></span>  <br/> |<span data-ttu-id="3f600-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="3f600-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="3f600-113">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3f600-113">Cell index:</span></span>  <br/> |<span data-ttu-id="3f600-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="3f600-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

