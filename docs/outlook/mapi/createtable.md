---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766366"
---
# <a name="createtable"></a><span data-ttu-id="b9b29-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="b9b29-103">CreateTable</span></span>

  
  
<span data-ttu-id="b9b29-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9b29-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9b29-105">Cria um identificador de objeto para um objeto [ITableData](itabledataiunknown.md) que pode ser usado para criar o conteúdo da tabela e de estruturas.</span><span class="sxs-lookup"><span data-stu-id="b9b29-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b9b29-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b9b29-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9b29-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b9b29-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b9b29-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b9b29-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9b29-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b9b29-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b9b29-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b9b29-110">Called by:</span></span>  <br/> |<span data-ttu-id="b9b29-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b9b29-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="b9b29-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9b29-112">Parameters</span></span>

 <span data-ttu-id="b9b29-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b9b29-113">_lpInterface_</span></span>
  
> <span data-ttu-id="b9b29-114">[in] Ponteiro para um identificador de interface (IID) para o objeto de dados de tabela.</span><span class="sxs-lookup"><span data-stu-id="b9b29-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="b9b29-115">O identificador de interface válido é IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="b9b29-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="b9b29-116">Passar NULL no parâmetro _lpInterface_ também fará com que o objeto de dados de tabela retornado no parâmetro _lppTableData_ para ser convertido para a interface padrão para um objeto de dados de tabela.</span><span class="sxs-lookup"><span data-stu-id="b9b29-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="b9b29-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b9b29-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="b9b29-118">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="b9b29-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="b9b29-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b9b29-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="b9b29-120">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="b9b29-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="b9b29-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="b9b29-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="b9b29-122">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="b9b29-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="b9b29-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="b9b29-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="b9b29-124">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b9b29-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="b9b29-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="b9b29-125">_ulTableType_</span></span>
  
> <span data-ttu-id="b9b29-126">[in] Um tipo de tabela que está disponível para um aplicativo cliente ou de um provedor de serviços como parte dos dados retorno [IMAPITable::GetStatus](imapitable-getstatus.md) em seus modos de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="b9b29-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="b9b29-127">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b9b29-127">Possible values are:</span></span> 
    
<span data-ttu-id="b9b29-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="b9b29-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="b9b29-129">O conteúdo da tabela é dinâmico e pode alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="b9b29-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="b9b29-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="b9b29-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="b9b29-131">As linhas da tabela são corrigidas, mas os valores nessas linhas são dinâmicos e podem alterar como as alterações de dados subjacente.</span><span class="sxs-lookup"><span data-stu-id="b9b29-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="b9b29-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="b9b29-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="b9b29-133">A tabela é estática e o conteúdo não é alterados quando os dados subjacentes forem alterados.</span><span class="sxs-lookup"><span data-stu-id="b9b29-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="b9b29-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="b9b29-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="b9b29-135">[in] Número de índice da coluna para uso ao alterar os dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="b9b29-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="b9b29-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="b9b29-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="b9b29-137">[in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades necessárias na tabela para o qual o objeto contém dados.</span><span class="sxs-lookup"><span data-stu-id="b9b29-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="b9b29-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="b9b29-138">_lppTableData_</span></span>
  
> <span data-ttu-id="b9b29-139">[out] Ponteiro para um ponteiro para o objeto de dados de tabela retornada.</span><span class="sxs-lookup"><span data-stu-id="b9b29-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b9b29-140">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b9b29-140">Return value</span></span>

<span data-ttu-id="b9b29-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9b29-141">S_OK</span></span> 
  
> <span data-ttu-id="b9b29-142">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="b9b29-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b9b29-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9b29-143">Remarks</span></span>

<span data-ttu-id="b9b29-144">Os parâmetros de entrada _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ apontam para o [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e funções [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b9b29-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="b9b29-145">Um aplicativo cliente chamar **CreateTable** passa em ponteiros para as funções MAPI apenas nomeadas; um provedor de serviços passa os ponteiros para essas funções que ele recebidas em sua chamada de inicialização ou recuperadas com uma chamada ao método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="b9b29-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9b29-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9b29-146">See also</span></span>



[<span data-ttu-id="b9b29-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9b29-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

