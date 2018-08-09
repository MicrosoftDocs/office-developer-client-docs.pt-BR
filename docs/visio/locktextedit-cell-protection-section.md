---
title: Célula LockTextEdit (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Protege o texto de uma forma impedindo-o de ser editado.
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772268"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="f3619-103">Célula LockTextEdit (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="f3619-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="f3619-104">Protege o texto de uma forma impedindo-o de ser editado.</span><span class="sxs-lookup"><span data-stu-id="f3619-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="f3619-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f3619-105">**Value**</span></span>|<span data-ttu-id="f3619-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f3619-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3619-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f3619-107">TRUE</span></span>  <br/> |<span data-ttu-id="f3619-108">O texto não pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="f3619-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="f3619-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="f3619-109">FALSE</span></span>  <br/> | <span data-ttu-id="f3619-110">O texto pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="f3619-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3619-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3619-111">Remarks</span></span>

<span data-ttu-id="f3619-112">Também é possível formatar o texto aplicando um estilo na caixa de diálogo **Texto** (na guia **Página Inicial**, clique em na seta **Fonte**).</span><span class="sxs-lookup"><span data-stu-id="f3619-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="f3619-113">Para obter uma referência para a célula LockTextEdit pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f3619-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3619-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f3619-114">Cell name:</span></span>  <br/> | <span data-ttu-id="f3619-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="f3619-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="f3619-116">Para obter uma referência para a célula LockTextEdit pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f3619-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f3619-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f3619-117">Section index:</span></span>  <br/> |<span data-ttu-id="f3619-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f3619-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f3619-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f3619-119">Row index:</span></span>  <br/> |<span data-ttu-id="f3619-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f3619-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f3619-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f3619-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f3619-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="f3619-122">**visLockTextEdit**</span></span> <br/> |
   
