---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410431"
---
# <a name="srow"></a><span data-ttu-id="bb56a-103">SRow</span><span class="sxs-lookup"><span data-stu-id="bb56a-103">SRow</span></span>

<span data-ttu-id="bb56a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb56a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb56a-105">Descreve uma linha de uma tabela que contém propriedades selecionadas para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="bb56a-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb56a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bb56a-106">Header file:</span></span>  <br/> |<span data-ttu-id="bb56a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bb56a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="bb56a-108">Members</span><span class="sxs-lookup"><span data-stu-id="bb56a-108">Members</span></span>

<span data-ttu-id="bb56a-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="bb56a-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="bb56a-110">Preenchimento de bytes para alinhar corretamente os valores de propriedade apontados pelo **membro lpProps.**</span><span class="sxs-lookup"><span data-stu-id="bb56a-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="bb56a-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bb56a-111">**cValues**</span></span>
  
> <span data-ttu-id="bb56a-112">Contagem de valores de propriedade apontados **por lpProps**.</span><span class="sxs-lookup"><span data-stu-id="bb56a-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="bb56a-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="bb56a-113">**lpProps**</span></span>
  
> <span data-ttu-id="bb56a-114">Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) que descrevem os valores de propriedade para as colunas na linha.</span><span class="sxs-lookup"><span data-stu-id="bb56a-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bb56a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb56a-115">Remarks</span></span>

<span data-ttu-id="bb56a-116">Uma **estrutura SRow** descreve uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="bb56a-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="bb56a-117">Ele está incluído na estrutura [TABLE_NOTIFICATION](table_notification.md) que acompanha uma notificação de tabela.</span><span class="sxs-lookup"><span data-stu-id="bb56a-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="bb56a-118">**As estruturas SRow** são usadas nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="bb56a-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="bb56a-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bb56a-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="bb56a-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bb56a-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="bb56a-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bb56a-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="bb56a-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="bb56a-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="bb56a-123">[ITableData : IUnknown](itabledataiunknown.md) (muitos métodos)</span><span class="sxs-lookup"><span data-stu-id="bb56a-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="bb56a-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="bb56a-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="bb56a-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="bb56a-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="bb56a-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="bb56a-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="bb56a-127">Quando mais de uma linha precisa ser descrita, uma [estrutura SRowSet](srowset.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="bb56a-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="bb56a-128">Uma **estrutura SRowSet** contém uma matriz de **estruturas SRow** e uma contagem de estruturas na matriz.</span><span class="sxs-lookup"><span data-stu-id="bb56a-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="bb56a-129">A ilustração a seguir mostra a relação entre uma **SRow** e uma **estrutura de dados SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="bb56a-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="bb56a-130">**Relationship between SRow and SRowSet**</span><span class="sxs-lookup"><span data-stu-id="bb56a-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="bb56a-131">![Relação entre SRow e SRowSet](media/amapi_17.gif "Relationship entre SRow e SRowSet")</span><span class="sxs-lookup"><span data-stu-id="bb56a-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="bb56a-132">**As estruturas SRow** são definidas da mesma forma que [as estruturas ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="bb56a-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="bb56a-133">Portanto, uma linha de uma tabela de destinatários e uma entrada em uma lista de endereços podem ser tratadas da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="bb56a-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="bb56a-134">Para obter informações sobre como a memória para estruturas **SRow** deve ser alocada, consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="bb56a-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bb56a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb56a-135">See also</span></span>

- [<span data-ttu-id="bb56a-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="bb56a-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="bb56a-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bb56a-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="bb56a-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="bb56a-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="bb56a-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bb56a-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="bb56a-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="bb56a-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="bb56a-141">Gerenciando memória para estruturas ADRLIST e SRowSet</span><span class="sxs-lookup"><span data-stu-id="bb56a-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

