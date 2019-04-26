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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360225"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="b855f-103">Célula de Descrição (Seção Ação Marcas)</span><span class="sxs-lookup"><span data-stu-id="b855f-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="b855f-104">Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.</span><span class="sxs-lookup"><span data-stu-id="b855f-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b855f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b855f-105">Remarks</span></span>

<span data-ttu-id="b855f-106">Para obter uma referência à célula Descrição pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="b855f-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b855f-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b855f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b855f-108">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b855f-108">SmartTags.</span></span>  <span data-ttu-id="b855f-109">*nome*  .Descrição           onde MarcasInteligentes.</span><span class="sxs-lookup"><span data-stu-id="b855f-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="b855f-110">*nome*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="b855f-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="b855f-111">Para obter uma referência à célula Description pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b855f-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b855f-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b855f-112">Section index:</span></span>  <br/> |<span data-ttu-id="b855f-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="b855f-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="b855f-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b855f-114">Row index:</span></span>  <br/> |<span data-ttu-id="b855f-115">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b855f-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b855f-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="b855f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b855f-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="b855f-117">**visSmartTagDescription**</span></span> <br/> |
   

