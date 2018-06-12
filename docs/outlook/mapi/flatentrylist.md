---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766563"
---
# <a name="flatentrylist"></a><span data-ttu-id="7ab67-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="7ab67-103">FLATENTRYLIST</span></span>

<span data-ttu-id="7ab67-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ab67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ab67-105">Contém uma matriz de estruturas [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="7ab67-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ab67-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7ab67-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ab67-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ab67-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7ab67-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="7ab67-108">Related macros:</span></span>  <br/> |<span data-ttu-id="7ab67-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="7ab67-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="7ab67-110">Membros</span><span class="sxs-lookup"><span data-stu-id="7ab67-110">Members</span></span>

<span data-ttu-id="7ab67-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="7ab67-111">**cEntries**</span></span>
  
> <span data-ttu-id="7ab67-112">Contagem de estruturas **FLATENTRY** na matriz descrito pelo membro **abEntries** .</span><span class="sxs-lookup"><span data-stu-id="7ab67-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="7ab67-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="7ab67-113">**cbEntries**</span></span>
  
> <span data-ttu-id="7ab67-114">Contagem de bytes na matriz descrita por **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="7ab67-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="7ab67-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="7ab67-115">**abEntries**</span></span>
  
> <span data-ttu-id="7ab67-116">Matriz de bytes que contém uma ou mais estruturas **FLATENTRY** , organizada ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="7ab67-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7ab67-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7ab67-117">Remarks</span></span>

<span data-ttu-id="7ab67-118">Na matriz **abEntries** , cada estrutura **FLATENTRY** é alinhada em um limite naturalmente alinhado.</span><span class="sxs-lookup"><span data-stu-id="7ab67-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="7ab67-119">Bytes extras são incluídos como preenchimento para tornar o alinhamento certeza natural entre qualquer duas estruturas **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="7ab67-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="7ab67-120">A estrutura **FLATENTRY** primeira na matriz é sempre alinhada corretamente porque o deslocamento do membro **abEntries** é 8.</span><span class="sxs-lookup"><span data-stu-id="7ab67-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="7ab67-121">Para calcular o deslocamento da próxima estrutura, use o tamanho da primeira entrada arredondado para cima até o próximo múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="7ab67-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="7ab67-122">Use a macro [CbFLATENTRY](cbflatentry.md) para calcular o tamanho de uma estrutura **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="7ab67-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="7ab67-123">Por exemplo, a estrutura **FLATENTRY** segunda é iniciado em um deslocamento que consiste o deslocamento da primeira entrada mais o comprimento da primeira entrada arredondado para o próximo de quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="7ab67-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="7ab67-124">O comprimento da primeira entrada é o comprimento da sua lista de membros **cb** mais o comprimento do seu membro **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="7ab67-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="7ab67-125">O exemplo de código a seguir indica como compute deslocamentos em uma estrutura **FLATENTRYLIST** .</span><span class="sxs-lookup"><span data-stu-id="7ab67-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="7ab67-126">Suponha que _lpFlatEntry_ é um ponteiro para a estrutura primeiro na lista.</span><span class="sxs-lookup"><span data-stu-id="7ab67-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="7ab67-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ab67-127">See also</span></span>

- [<span data-ttu-id="7ab67-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="7ab67-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="7ab67-129">Propriedade canônico de PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="7ab67-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="7ab67-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="7ab67-130">MAPI Structures</span></span>](mapi-structures.md)

