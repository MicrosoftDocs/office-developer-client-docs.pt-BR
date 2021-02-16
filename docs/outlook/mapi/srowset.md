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
# <a name="srowset"></a><span data-ttu-id="2b107-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2b107-103">SRowSet</span></span>

  
  
<span data-ttu-id="2b107-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b107-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b107-105">Contém uma matriz de [estruturas SRow.](srow.md)</span><span class="sxs-lookup"><span data-stu-id="2b107-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="2b107-106">Cada **estrutura SRow** descreve uma linha de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2b107-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b107-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2b107-107">Header file:</span></span>  <br/> |<span data-ttu-id="2b107-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b107-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b107-109">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="2b107-109">Related macros:</span></span>  <br/> |<span data-ttu-id="2b107-110">[CbNewsRowSet](cbnewsrowset.md), [CbsRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="2b107-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="2b107-111">Members</span><span class="sxs-lookup"><span data-stu-id="2b107-111">Members</span></span>

 <span data-ttu-id="2b107-112">**cRows**</span><span class="sxs-lookup"><span data-stu-id="2b107-112">**cRows**</span></span>
  
> <span data-ttu-id="2b107-113">Contagem de **estruturas SRow** no **membro aRow.**</span><span class="sxs-lookup"><span data-stu-id="2b107-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="2b107-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="2b107-114">**aRow**</span></span>
  
> <span data-ttu-id="2b107-115">Matriz de **estruturas SRow.**</span><span class="sxs-lookup"><span data-stu-id="2b107-115">Array of **SRow** structures.</span></span> <span data-ttu-id="2b107-116">Há uma estrutura para cada linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="2b107-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b107-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b107-117">Remarks</span></span>

<span data-ttu-id="2b107-118">Uma **estrutura SRowSet** é usada para descrever várias linhas de dados de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2b107-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="2b107-119">**Estruturas SRowSet** são usadas nos métodos de interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e [IMAPITable,](imapitableiunknown.md) além das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="2b107-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="2b107-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="2b107-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="2b107-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="2b107-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="2b107-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2b107-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="2b107-123">**As estruturas SRowSet** são definidas da mesma forma que estruturas [ADRLIST](adrlist.md) para permitir que as linhas de uma tabela de destinatários e as entradas em uma lista de endereços sejam tratadas da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="2b107-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="2b107-124">Tanto estruturas **SRowSet** quanto **estruturas ADRLIST** podem ser passadas para métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="2b107-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="2b107-125">Além disso, as regras de alocação de memória **para estruturas SRowSet** são as mesmas para **estruturas ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="2b107-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="2b107-126">Para resumir, cada estrutura [SPropValue](spropvalue.md) na matriz apontada pelo membro **lpProps** de cada linha no conjunto de linhas deve ser alocada separadamente usando [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2b107-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="2b107-127">Cada estrutura de valores de propriedade também deve ser desaloçada usando [MAPIFreeBuffer](mapifreebuffer.md) antes da desalocação de sua estrutura **SRowSet** para que os ponteiros para as estruturas **SPropValue** alocadas não sejam perdidos.</span><span class="sxs-lookup"><span data-stu-id="2b107-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="2b107-128">A memória alocada de uma linha pode ser preservada e reutilizada fora do contexto da **estrutura SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="2b107-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="2b107-129">Para obter mais informações sobre como a memória para estruturas **SRowSet** deve ser alocada, consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2b107-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b107-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b107-130">See also</span></span>



[<span data-ttu-id="2b107-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2b107-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="2b107-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2b107-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2b107-133">SRow</span><span class="sxs-lookup"><span data-stu-id="2b107-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="2b107-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2b107-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2b107-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2b107-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="2b107-136">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2b107-136">MAPI Structures</span></span>](mapi-structures.md)

