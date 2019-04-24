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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282730"
---
# <a name="sizeddtblgroupbox"></a><span data-ttu-id="ccb48-103">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="ccb48-103">SizedDtblGroupBox</span></span>

<span data-ttu-id="ccb48-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb48-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLGROUPBOX](dtblgroupbox.md) para descrever um controle de caixa de grupo e um rótulo de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="ccb48-105">Creates a named structure that includes a [DTBLGROUPBOX](dtblgroupbox.md) structure for describing a group box control and a label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ccb48-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ccb48-106">Header file:</span></span>  <br/> |<span data-ttu-id="ccb48-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ccb48-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ccb48-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="ccb48-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ccb48-109">**DTBLGROUPBOX**</span><span class="sxs-lookup"><span data-stu-id="ccb48-109">**DTBLGROUPBOX**</span></span> <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="ccb48-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb48-110">Parameters</span></span>

<span data-ttu-id="ccb48-111">_n_</span><span class="sxs-lookup"><span data-stu-id="ccb48-111">_n_</span></span>
  
> <span data-ttu-id="ccb48-112">Comprimento do rótulo da caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="ccb48-112">Length of the group box's label.</span></span> 
    
<span data-ttu-id="ccb48-113">_u_</span><span class="sxs-lookup"><span data-stu-id="ccb48-113">_u_</span></span>
  
> <span data-ttu-id="ccb48-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ccb48-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ccb48-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccb48-115">Remarks</span></span>

<span data-ttu-id="ccb48-116">A macro **SizedDtblGroupBox** permite definir um controle de caixa de grupo quando o comprimento do rótulo é conhecido.</span><span class="sxs-lookup"><span data-stu-id="ccb48-116">The **SizedDtblGroupBox** macro lets you define a group box control when the length of the label is known.</span></span> <span data-ttu-id="ccb48-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="ccb48-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

<span data-ttu-id="ccb48-118">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblGroupBox** como um ponteiro de estrutura **DTBLGROUPBOX** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="ccb48-118">To use a pointer to the resulting structure from the **SizedDtblGroupBox** macro as a **DTBLGROUPBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a><span data-ttu-id="ccb48-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb48-119">See also</span></span>

- [<span data-ttu-id="ccb48-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="ccb48-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="ccb48-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="ccb48-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

