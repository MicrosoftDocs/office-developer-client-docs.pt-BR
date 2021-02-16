---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0a9bda8831f4a38b62d71a54115c40bb3374d97d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419314"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="e037a-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="e037a-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="e037a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e037a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e037a-105">Cria uma estrutura nomeada que inclui uma [estrutura DTBLGROUPBOX](dtblgroupbox.md) para descrever um controle de caixa de grupo e um rótulo de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="e037a-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e037a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e037a-106">Header file:</span></span>  <br/> |<span data-ttu-id="e037a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e037a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e037a-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="e037a-108">Related structure:</span></span>  <br/> |<span data-ttu-id="e037a-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="e037a-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="e037a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e037a-110">Parameters</span></span>

<span data-ttu-id="e037a-111">_n_</span><span class="sxs-lookup"><span data-stu-id="e037a-111">_n_</span></span>
  
> <span data-ttu-id="e037a-112">Comprimento do rótulo da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="e037a-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="e037a-113">_u_</span><span class="sxs-lookup"><span data-stu-id="e037a-113">_u_</span></span>
  
> <span data-ttu-id="e037a-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="e037a-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e037a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e037a-115">Remarks</span></span>

<span data-ttu-id="e037a-116">A macro **SizedDtblGroupBox** permite definir um controle de caixa de grupo quando o tamanho do rótulo for conhecido.</span><span class="sxs-lookup"><span data-stu-id="e037a-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="e037a-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="e037a-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="e037a-118">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblGroupBox** como um ponteiro de **estrutura DTBLGROUPBOX,** execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="e037a-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="e037a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e037a-119">See also</span></span>

- [<span data-ttu-id="e037a-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="e037a-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="e037a-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="e037a-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

