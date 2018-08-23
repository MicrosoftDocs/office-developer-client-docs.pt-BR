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
ms.openlocfilehash: 82fa1b0af504cc4774b1dc077a6ef48378740d26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580674"
---
# <a name="srowset"></a><span data-ttu-id="2af5c-103">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2af5c-103">SRowSet</span></span>

  
  
<span data-ttu-id="2af5c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af5c-105">Contém uma matriz de estruturas de [SRow](srow.md) .</span><span class="sxs-lookup"><span data-stu-id="2af5c-105">Contains an array of [SRow](srow.md) structures.</span></span> <span data-ttu-id="2af5c-106">Cada estrutura **SRow** descreve uma linha de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2af5c-106">Each **SRow** structure describes a row from a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2af5c-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2af5c-107">Header file:</span></span>  <br/> |<span data-ttu-id="2af5c-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2af5c-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2af5c-109">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="2af5c-109">Related macros:</span></span>  <br/> |<span data-ttu-id="2af5c-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span><span class="sxs-lookup"><span data-stu-id="2af5c-110">[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md)</span></span> <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a><span data-ttu-id="2af5c-111">Members</span><span class="sxs-lookup"><span data-stu-id="2af5c-111">Members</span></span>

 <span data-ttu-id="2af5c-112">**Pássaros**</span><span class="sxs-lookup"><span data-stu-id="2af5c-112">**cRows**</span></span>
  
> <span data-ttu-id="2af5c-113">Contagem de estruturas de **SRow** no membro **aRow** .</span><span class="sxs-lookup"><span data-stu-id="2af5c-113">Count of **SRow** structures in the **aRow** member.</span></span> 
    
 <span data-ttu-id="2af5c-114">**aRow**</span><span class="sxs-lookup"><span data-stu-id="2af5c-114">**aRow**</span></span>
  
> <span data-ttu-id="2af5c-115">Matriz de estruturas de **SRow** .</span><span class="sxs-lookup"><span data-stu-id="2af5c-115">Array of **SRow** structures.</span></span> <span data-ttu-id="2af5c-116">Não há uma estrutura para cada linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="2af5c-116">There is one structure for each row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2af5c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2af5c-117">Remarks</span></span>

<span data-ttu-id="2af5c-118">Uma estrutura de **SRowSet** é usada para descrever a várias linhas de dados de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2af5c-118">An **SRowSet** structure is used to describe multiple rows of data from a table.</span></span> <span data-ttu-id="2af5c-119">Estruturas de **SRowSet** são usadas nos métodos de interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e [IMAPITable](imapitableiunknown.md) , além das funções a seguir:</span><span class="sxs-lookup"><span data-stu-id="2af5c-119">**SRowSet** structures are used in the [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md), and [IMAPITable](imapitableiunknown.md) interface methods, in addition to the following functions:</span></span> 
  
- [<span data-ttu-id="2af5c-120">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="2af5c-120">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
- [<span data-ttu-id="2af5c-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="2af5c-121">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="2af5c-122">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2af5c-122">FreeProws</span></span>](freeprows.md)
    
 <span data-ttu-id="2af5c-123">Estruturas de **SRowSet** são definidas da mesma forma estruturas [ADRLIST](adrlist.md) para permitir que as linhas de uma tabela de destinatário e as entradas em uma lista de endereços a ser tratados da mesma.</span><span class="sxs-lookup"><span data-stu-id="2af5c-123">**SRowSet** structures are defined the same as [ADRLIST](adrlist.md) structures to allow the rows of a recipient table and the entries in an address list to be treated the same.</span></span> <span data-ttu-id="2af5c-124">Estruturas de **SRowSet** e de estruturas **ADRLIST** podem ser passadas para os métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="2af5c-124">Both **SRowSet** structures and **ADRLIST** structures can be passed to methods such as [IMessage::ModifyRecipients](imessage-modifyrecipients.md) and [IAddrBook::Address](iaddrbook-address.md).</span></span> 
  
<span data-ttu-id="2af5c-125">Além disso, as regras de alocação de memória para as estruturas de **SRowSet** são iguais às propriedades de estruturas **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="2af5c-125">Also, the rules for memory allocation for **SRowSet** structures are the same as for **ADRLIST** structures.</span></span> <span data-ttu-id="2af5c-126">Resumindo, cada estrutura [SPropValue](spropvalue.md) na matriz apontada para pelo membro de cada linha na linha **lpProps** definir deve ser alocada separadamente usando [MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2af5c-126">To summarize, each [SPropValue](spropvalue.md) structure in the array pointed to by the **lpProps** member of each row in the row set must be allocated separately using [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span> <span data-ttu-id="2af5c-127">Cada estrutura de valor de propriedade também deve ser desalocada usando [MAPIFreeBuffer](mapifreebuffer.md) antes da desalocação de sua estrutura de **SRowSet** para que os ponteiros para as estruturas de **SPropValue** alocados não são perdidos.</span><span class="sxs-lookup"><span data-stu-id="2af5c-127">Each property value structure must also be deallocated using [MAPIFreeBuffer](mapifreebuffer.md) before the deallocation of its **SRowSet** structure so that pointers to the allocated **SPropValue** structures are not lost.</span></span> <span data-ttu-id="2af5c-128">Uma linha do alocar memória podem então ser preservada e reutilizada fora do contexto da estrutura **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="2af5c-128">A row's allocated memory can then be preserved and reused outside the context of the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="2af5c-129">Para obter mais informações sobre como a memória para as estruturas de **SRowSet** deve ser alocada, consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2af5c-129">For more information about how the memory for **SRowSet** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2af5c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2af5c-130">See also</span></span>



[<span data-ttu-id="2af5c-131">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2af5c-131">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="2af5c-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2af5c-132">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="2af5c-133">SRow</span><span class="sxs-lookup"><span data-stu-id="2af5c-133">SRow</span></span>](srow.md)
  
[<span data-ttu-id="2af5c-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2af5c-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2af5c-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2af5c-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="2af5c-136">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2af5c-136">MAPI Structures</span></span>](mapi-structures.md)

