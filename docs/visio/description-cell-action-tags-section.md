---
title: Célula Description (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415758"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="3ba77-103">Célula de Descrição (Seção Ação Marcas)</span><span class="sxs-lookup"><span data-stu-id="3ba77-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="3ba77-104">Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.</span><span class="sxs-lookup"><span data-stu-id="3ba77-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ba77-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ba77-105">Remarks</span></span>

<span data-ttu-id="3ba77-106">Para obter uma referência à célula Descrição pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="3ba77-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ba77-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3ba77-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3ba77-108">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="3ba77-108">SmartTags.</span></span>  <span data-ttu-id="3ba77-109">*nome*  .Descrição           onde MarcasInteligentes.</span><span class="sxs-lookup"><span data-stu-id="3ba77-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="3ba77-110">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="3ba77-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="3ba77-111">Para obter uma referência à célula Description pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3ba77-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3ba77-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3ba77-112">Section index:</span></span>  <br/> |<span data-ttu-id="3ba77-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="3ba77-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="3ba77-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="3ba77-114">Row index:</span></span>  <br/> |<span data-ttu-id="3ba77-115">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3ba77-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3ba77-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="3ba77-116">Cell index:</span></span>  <br/> |<span data-ttu-id="3ba77-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="3ba77-117">**visSmartTagDescription**</span></span> <br/> |
   

