---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407253"
---
# <a name="srowset"></a><span data-ttu-id="5a22b-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="5a22b-103">SRowSet</span></span>

  
  
<span data-ttu-id="5a22b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a22b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a22b-105">Contém uma matriz de estruturas [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="5a22b-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="5a22b-106">Cada estrutura **SRow** descreve uma linha de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5a22b-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a22b-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5a22b-107">Header file:</span></span>  <br/> |<span data-ttu-id="5a22b-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5a22b-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a22b-109">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="5a22b-109">Related macros:</span></span>  <br/> |<span data-ttu-id="5a22b-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="5a22b-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="5a22b-111">Members</span><span class="sxs-lookup"><span data-stu-id="5a22b-111">Members</span></span>

 <span data-ttu-id="5a22b-112">**Galinha**</span><span class="sxs-lookup"><span data-stu-id="5a22b-112">**cRows**</span></span>
  
> <span data-ttu-id="5a22b-113">Contagem de estruturas **SRow** no membro **aRow** .</span><span class="sxs-lookup"><span data-stu-id="5a22b-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="5a22b-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="5a22b-114">**aRow**</span></span>
  
> <span data-ttu-id="5a22b-115">Matriz de estruturas **SRow** .</span><span class="sxs-lookup"><span data-stu-id="5a22b-115">Array of **SRow** structures.</span></span> <span data-ttu-id="5a22b-116">Há uma estrutura para cada linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="5a22b-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a22b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a22b-117">Remarks</span></span>

<span data-ttu-id="5a22b-118">Uma estrutura **SRowSet** é usada para descrever várias linhas de dados de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="5a22b-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="5a22b-119">As estruturas **SRowSet** são usadas nos métodos de interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e IMAPITable, além das seguintes funções: [](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="5a22b-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="5a22b-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="5a22b-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="5a22b-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="5a22b-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="5a22b-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="5a22b-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="5a22b-123">As estruturas **SRowSet** são definidas da mesma forma que as estruturas [das ADRLIST](adrlist.md) para permitir que as linhas de uma tabela de destinatários e as entradas em uma lista de endereços sejam tratadas da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="5a22b-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="5a22b-124">Tanto estruturas **SRowSet** quanto estruturas **das ADRLIST** podem ser passadas para métodos como [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook:: address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="5a22b-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="5a22b-125">Além disso, as regras para a alocação de memória para estruturas **SRowSet** são as mesmas que as estruturas **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="5a22b-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="5a22b-126">Para resumir, cada estrutura [SPropValue](spropvalue.md) na matriz apontada pelo membro **lpProps** de cada linha no conjunto de linhas deve ser alocaDa separadamente usando o [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="5a22b-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="5a22b-127">Cada estrutura de valor de propriedade também deve ser desalocada usando [MAPIFreeBuffer](mapifreebuffer.md) antes da desalocação de sua estrutura **SRowSet** para que os ponteiros para as estruturas **SPropValue** alocadas não sejam perdidos.</span><span class="sxs-lookup"><span data-stu-id="5a22b-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="5a22b-128">A memória alocada de uma linha pode ser preservada e reutilizada fora do contexto da estrutura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="5a22b-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="5a22b-129">Para obter mais informações sobre como a memória para estruturas do **SRowSet** devem ser alocadas, consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="5a22b-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a22b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a22b-130">See also</span></span>



[<span data-ttu-id="5a22b-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="5a22b-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="5a22b-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5a22b-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5a22b-133">SRow</span><span class="sxs-lookup"><span data-stu-id="5a22b-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="5a22b-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="5a22b-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="5a22b-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="5a22b-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="5a22b-136">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5a22b-136">MAPI Structures</span></span>](mapi-structures.md)

