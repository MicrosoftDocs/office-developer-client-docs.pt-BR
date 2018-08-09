---
title: Célula NoCoauth (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772417"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="c7ea5-103">Célula NoCoauth (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="c7ea5-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="c7ea5-104">Define se um documento armazenado em um servidor do Microsoft SharePoint 2013 ou Microsoft OneDrive pode ser editado por vários autores simultaneamente em uma sessão de coautoria.</span><span class="sxs-lookup"><span data-stu-id="c7ea5-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="c7ea5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c7ea5-105">**Value**</span></span>|<span data-ttu-id="c7ea5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7ea5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7ea5-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c7ea5-107">TRUE</span></span>  <br/> |<span data-ttu-id="c7ea5-108">O documento não pode ser coautor e está bloqueado para edição quando estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="c7ea5-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="c7ea5-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="c7ea5-109">FALSE</span></span>  <br/> |<span data-ttu-id="c7ea5-110">Pode ser coautor do documento.</span><span class="sxs-lookup"><span data-stu-id="c7ea5-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7ea5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7ea5-111">Remarks</span></span>

<span data-ttu-id="c7ea5-112">Para fazer referência à célula **NoCoauth** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7ea5-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c7ea5-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="c7ea5-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="c7ea5-115">Para obter uma referência à célula **NoCoauth** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7ea5-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-116">Section index:</span></span>  <br/> |<span data-ttu-id="c7ea5-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7ea5-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7ea5-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-118">Row index:</span></span>  <br/> |<span data-ttu-id="c7ea5-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c7ea5-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="c7ea5-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c7ea5-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c7ea5-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="c7ea5-121">**visDocNoCoauth**</span></span> <br/> |
   

