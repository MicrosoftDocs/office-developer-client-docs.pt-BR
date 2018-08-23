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
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579120"
---
# <a name="srow"></a><span data-ttu-id="2af33-103">SRow</span><span class="sxs-lookup"><span data-stu-id="2af33-103">SRow</span></span>

<span data-ttu-id="2af33-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af33-105">Descreve uma linha de uma tabela que contém as propriedades selecionadas para um objeto específico.</span><span class="sxs-lookup"><span data-stu-id="2af33-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2af33-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2af33-106">Header file:</span></span>  <br/> |<span data-ttu-id="2af33-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2af33-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="2af33-108">Members</span><span class="sxs-lookup"><span data-stu-id="2af33-108">Members</span></span>

<span data-ttu-id="2af33-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="2af33-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="2af33-110">Preenchimento bytes para alinhar adequadamente os valores de propriedade apontado pelo membro **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="2af33-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="2af33-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2af33-111">**cValues**</span></span>
  
> <span data-ttu-id="2af33-112">Contagem de valores de propriedade apontado pela **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="2af33-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="2af33-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="2af33-113">**lpProps**</span></span>
  
> <span data-ttu-id="2af33-114">Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que descrevem os valores de propriedade para as colunas na linha.</span><span class="sxs-lookup"><span data-stu-id="2af33-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2af33-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2af33-115">Remarks</span></span>

<span data-ttu-id="2af33-116">Uma estrutura **SRow** descreve uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="2af33-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="2af33-117">Ele está incluído na estrutura [TABLE_NOTIFICATION](table_notification.md) que acompanha uma notificação de tabela.</span><span class="sxs-lookup"><span data-stu-id="2af33-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="2af33-118">Estruturas de **SRow** são usadas nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="2af33-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="2af33-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2af33-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="2af33-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="2af33-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="2af33-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2af33-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="2af33-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="2af33-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="2af33-123">[ITableData: IUnknown](itabledataiunknown.md) (muitos métodos)</span><span class="sxs-lookup"><span data-stu-id="2af33-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="2af33-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="2af33-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="2af33-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2af33-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="2af33-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="2af33-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="2af33-127">Quando mais de uma linha precisa ser descrito, uma estrutura de [SRowSet](srowset.md) é usada.</span><span class="sxs-lookup"><span data-stu-id="2af33-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="2af33-128">Uma estrutura **SRowSet** contém uma matriz de estruturas de **SRow** e uma contagem de estruturas na matriz.</span><span class="sxs-lookup"><span data-stu-id="2af33-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="2af33-129">A ilustração a seguir mostra a relação entre um **SRow** e uma estrutura de dados **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="2af33-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="2af33-130">**Relationship between SRow and SRowSet**</span><span class="sxs-lookup"><span data-stu-id="2af33-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="2af33-131">![Relação entre SRow e SRowSet] (media/amapi_17.gif "Relação entre SRow e SRowSet")</span><span class="sxs-lookup"><span data-stu-id="2af33-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="2af33-132">Estruturas de **SRow** são definidas iguais [ADRENTRY](adrentry.md) estruturas.</span><span class="sxs-lookup"><span data-stu-id="2af33-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="2af33-133">Portanto, uma linha de uma tabela de destinatário e uma entrada em uma lista de endereços pode ser tratados da mesma.</span><span class="sxs-lookup"><span data-stu-id="2af33-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="2af33-134">Para obter informações sobre como a memória para as estruturas de **SRow** deve ser alocada, consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2af33-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2af33-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2af33-135">See also</span></span>

- [<span data-ttu-id="2af33-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2af33-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="2af33-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2af33-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="2af33-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="2af33-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="2af33-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="2af33-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="2af33-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2af33-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="2af33-141">Gerenciar memória das estruturas ADRLIST e SRowSet</span><span class="sxs-lookup"><span data-stu-id="2af33-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

