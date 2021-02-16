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
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435009"
---
# <a name="createtable"></a><span data-ttu-id="fe2e8-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="fe2e8-103">CreateTable</span></span>

  
  
<span data-ttu-id="fe2e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe2e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe2e8-105">Cria estruturas e um identificador de objeto para [um objeto ITableData](itabledataiunknown.md) que pode ser usado para criar conteúdo de tabela.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe2e8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fe2e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe2e8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fe2e8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fe2e8-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="fe2e8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe2e8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe2e8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fe2e8-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="fe2e8-110">Called by:</span></span>  <br/> |<span data-ttu-id="fe2e8-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="fe2e8-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="fe2e8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe2e8-112">Parameters</span></span>

 <span data-ttu-id="fe2e8-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-113">_lpInterface_</span></span>
  
> <span data-ttu-id="fe2e8-114">[in] Ponteiro para um IID (identificador de interface) para o objeto de dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="fe2e8-115">O identificador de interface válido é IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="fe2e8-116">Passar NULL no parâmetro  _lpInterface_ também faz com que o objeto de dados de tabela retornado no parâmetro  _lppTableData_ seja cast para a interface padrão de um objeto de dados de tabela.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="fe2e8-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="fe2e8-118">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="fe2e8-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="fe2e8-120">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="fe2e8-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="fe2e8-122">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="fe2e8-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="fe2e8-124">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="fe2e8-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-125">_ulTableType_</span></span>
  
> <span data-ttu-id="fe2e8-126">[in] Um tipo de tabela que está disponível para um aplicativo cliente ou provedor de serviços como parte do [IMAPITable::GetStatus](imapitable-getstatus.md) retorna dados em seus exibições de tabela.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="fe2e8-127">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="fe2e8-127">Possible values are:</span></span> 
    
<span data-ttu-id="fe2e8-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="fe2e8-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="fe2e8-129">O conteúdo do índice é dinâmico e pode mudar à medida que os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="fe2e8-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="fe2e8-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="fe2e8-131">As linhas na tabela são fixas, mas os valores nessas linhas são dinâmicos e podem mudar à medida que os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="fe2e8-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="fe2e8-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="fe2e8-133">A tabela é estática e o conteúdo não muda quando os dados subjacentes mudam.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="fe2e8-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="fe2e8-135">[in] Número de índice da coluna a ser usada ao alterar dados da tabela.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="fe2e8-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="fe2e8-137">[in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades necessárias na tabela para a qual o objeto contém dados.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="fe2e8-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="fe2e8-138">_lppTableData_</span></span>
  
> <span data-ttu-id="fe2e8-139">[out] Ponteiro para um ponteiro para o objeto de dados de tabela retornado.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fe2e8-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fe2e8-140">Return value</span></span>

<span data-ttu-id="fe2e8-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe2e8-141">S_OK</span></span> 
  
> <span data-ttu-id="fe2e8-142">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe2e8-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe2e8-143">Remarks</span></span>

<span data-ttu-id="fe2e8-144">Os parâmetros de entrada  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer,](mapifreebuffer.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fe2e8-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="fe2e8-145">Um aplicativo cliente que **chama CreateTable** passa ponteiros para as funções MAPI nomeadas; um provedor de serviços passa os ponteiros para essas funções recebidas em sua chamada de inicialização ou recuperadas com uma chamada para o método [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md)</span><span class="sxs-lookup"><span data-stu-id="fe2e8-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe2e8-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe2e8-146">See also</span></span>



[<span data-ttu-id="fe2e8-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe2e8-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

