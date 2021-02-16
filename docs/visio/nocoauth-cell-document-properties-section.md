---
title: Célula NoCoauth (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou no Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautor.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420511"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="abe11-103">Célula NoCoauth (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="abe11-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="abe11-104">Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou no Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautor.</span><span class="sxs-lookup"><span data-stu-id="abe11-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="abe11-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="abe11-105">**Value**</span></span>|<span data-ttu-id="abe11-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="abe11-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abe11-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="abe11-107">TRUE</span></span>  <br/> |<span data-ttu-id="abe11-108">O documento não pode ser coautor e está bloqueado para edição quando aberto.</span><span class="sxs-lookup"><span data-stu-id="abe11-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="abe11-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="abe11-109">FALSE</span></span>  <br/> |<span data-ttu-id="abe11-110">O documento pode ser coautor.</span><span class="sxs-lookup"><span data-stu-id="abe11-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abe11-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="abe11-111">Remarks</span></span>

<span data-ttu-id="abe11-112">Para fazer referência à célula **NoCoauth** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="abe11-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="abe11-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="abe11-113">Cell name:</span></span>  <br/> | <span data-ttu-id="abe11-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="abe11-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="abe11-115">Para fazer referência à célula **NoCoauth** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="abe11-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="abe11-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="abe11-116">Section index:</span></span>  <br/> |<span data-ttu-id="abe11-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="abe11-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="abe11-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="abe11-118">Row index:</span></span>  <br/> |<span data-ttu-id="abe11-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="abe11-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="abe11-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="abe11-120">Cell index:</span></span>  <br/> |<span data-ttu-id="abe11-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="abe11-121">**visDocNoCoauth**</span></span> <br/> |
   

