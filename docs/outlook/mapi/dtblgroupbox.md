---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9295c37a46d3566089f708aaaa0b9fc3b5f30db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766478"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="b9783-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="b9783-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="b9783-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9783-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9783-105">Descreve um controle de caixa de grupo que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="b9783-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9783-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b9783-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9783-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9783-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b9783-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="b9783-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b9783-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="b9783-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="b9783-110">Members</span><span class="sxs-lookup"><span data-stu-id="b9783-110">Members</span></span>

 <span data-ttu-id="b9783-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="b9783-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="b9783-112">Posição na memória da sequência de caracteres que acompanha a caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="b9783-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="b9783-113">Se exibido, o rótulo aparece no lado superior, esquerdo da caixa.</span><span class="sxs-lookup"><span data-stu-id="b9783-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="b9783-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="b9783-114">**ulFlags**</span></span>
  
> <span data-ttu-id="b9783-115">Bitmask dos sinalizadores usados para designar o formato do rótulo apontado pelo membro **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="b9783-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="b9783-116">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="b9783-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="b9783-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b9783-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b9783-118">O rótulo está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="b9783-118">The label is in Unicode format.</span></span> <span data-ttu-id="b9783-119">Se o sinalizador MAPI_UNICODE não estiver definido, o rótulo está no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="b9783-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9783-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9783-120">Remarks</span></span>

<span data-ttu-id="b9783-121">Uma estrutura **DTBLGROUPBOX** descreve um controle de caixa de grupo que é usado para associar visualmente outros controles na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b9783-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="b9783-122">A técnica de realce envolve ao redor por uma caixa os outros controles.</span><span class="sxs-lookup"><span data-stu-id="b9783-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="b9783-123">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b9783-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="b9783-124">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="b9783-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b9783-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9783-125">See also</span></span>



[<span data-ttu-id="b9783-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="b9783-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="b9783-127">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b9783-127">MAPI Structures</span></span>](mapi-structures.md)

