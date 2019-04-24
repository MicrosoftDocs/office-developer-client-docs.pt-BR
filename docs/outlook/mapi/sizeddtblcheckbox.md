---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d23d56a27095497aedc64d7bbf5ffda266d0c97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282751"
---
# <a name="sizeddtblcheckbox"></a><span data-ttu-id="7c69b-103">SizedDtblCheckBox</span><span class="sxs-lookup"><span data-stu-id="7c69b-103">SizedDtblCheckBox</span></span>
 
<span data-ttu-id="7c69b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c69b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c69b-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLCHECKBOX](dtblcheckbox.md) para descrever um controle de caixa de seleção e um rótulo de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="7c69b-105">Creates a named structure that includes a [DTBLCHECKBOX](dtblcheckbox.md) structure for describing a check box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c69b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7c69b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c69b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c69b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7c69b-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7c69b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7c69b-109">**DTBLCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="7c69b-109">**DTBLCHECKBOX**</span></span> <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="7c69b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c69b-110">Parameters</span></span>

<span data-ttu-id="7c69b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="7c69b-111">_n_</span></span>
  
> <span data-ttu-id="7c69b-112">Comprimento do rótulo a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="7c69b-112">Length of the label to be included in the new structure.</span></span>
    
<span data-ttu-id="7c69b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="7c69b-113">_u_</span></span>
  
> <span data-ttu-id="7c69b-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="7c69b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c69b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c69b-115">Remarks</span></span>

<span data-ttu-id="7c69b-116">A macro **SizedDtblCheckBox** permite definir uma caixa de seleção quando o número de caracteres de rótulo é conhecido.</span><span class="sxs-lookup"><span data-stu-id="7c69b-116">The **SizedDtblCheckBox** macro lets you define a check box when the number of label characters is known.</span></span> <span data-ttu-id="7c69b-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="7c69b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

<span data-ttu-id="7c69b-118">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblCheckBox** como um ponteiro de estrutura **DTBLCHECKBOX** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="7c69b-118">To use a pointer to the resulting structure from the **SizedDtblCheckBox** macro as a **DTBLCHECKBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a><span data-ttu-id="7c69b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c69b-119">See also</span></span>

- [<span data-ttu-id="7c69b-120">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="7c69b-120">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="7c69b-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="7c69b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

