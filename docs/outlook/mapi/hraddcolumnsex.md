---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427476"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="147a4-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="147a4-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="147a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="147a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="147a4-105">Adiciona ou move colunas no início de uma tabela existente.</span><span class="sxs-lookup"><span data-stu-id="147a4-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="147a4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="147a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="147a4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="147a4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="147a4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="147a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="147a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="147a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="147a4-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="147a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="147a4-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="147a4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="147a4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="147a4-112">Parameters</span></span>

 <span data-ttu-id="147a4-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="147a4-113">_lptbl_</span></span>
  
> <span data-ttu-id="147a4-114">no Ponteiro para a tabela MAPI afetada.</span><span class="sxs-lookup"><span data-stu-id="147a4-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="147a4-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="147a4-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="147a4-116">no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade para as propriedades a serem adicionadas ou movidas para o início da tabela.</span><span class="sxs-lookup"><span data-stu-id="147a4-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="147a4-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="147a4-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="147a4-118">no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="147a4-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="147a4-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="147a4-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="147a4-120">no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="147a4-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="147a4-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="147a4-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="147a4-122">no Ponteiro para uma função de retorno de chamada fornecida pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="147a4-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="147a4-123">Se o parâmetro _lpfnFilterColumns_ estiver definido como nulo, nenhum retorno de chamada será feito.</span><span class="sxs-lookup"><span data-stu-id="147a4-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="147a4-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="147a4-124">_ptaga_</span></span>
  
> <span data-ttu-id="147a4-125">no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém a matriz de marcas de propriedade já existentes na tabela antes das propriedades serem adicionadas ou movidas para o início.</span><span class="sxs-lookup"><span data-stu-id="147a4-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="147a4-126">**HrAddColumnsEx** passa esse ponteiro como o parâmetro para a função de retorno de chamada indicada por _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="147a4-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="147a4-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="147a4-127">Return value</span></span>

<span data-ttu-id="147a4-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="147a4-128">S_OK</span></span> 
  
> <span data-ttu-id="147a4-129">A chamada foi bem-sucedida e as colunas especificadas foram movidas ou adicionadas.</span><span class="sxs-lookup"><span data-stu-id="147a4-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="147a4-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="147a4-130">Remarks</span></span>

<span data-ttu-id="147a4-131">As propriedades passadas para **HrAddColumnsEx** usando o parâmetro _lpproptagColumnsNew_ se tornam as primeiras propriedades expostas em chamadas subsequentes para o método IMAPITable [:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="147a4-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="147a4-132">Quaisquer propriedades anteriormente na tabela que não foram especificadas no parâmetro _lpproptagColumnsNew_ são expostas após todas as propriedades adicionadas e movidas.</span><span class="sxs-lookup"><span data-stu-id="147a4-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="147a4-133">Se qualquer propriedade da tabela estiver indefinida quando **QueryRows** for chamado, elas serão retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="147a4-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="147a4-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="147a4-134">Notes to callers</span></span>

<span data-ttu-id="147a4-135">A função **HrAddColumnsEx** permite que o chamador forneça uma função de retorno de chamada para filtrar as colunas que já estavam na tabela, por exemplo, para converter cadeias de caracteres do tipo de propriedade PT_UNICODE para PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="147a4-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="147a4-136">**HrAddColumnsEx** passa um ponteiro para o conjunto de colunas existente anteriormente como o parâmetro para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="147a4-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="147a4-137">A função de retorno de chamada pode alterar os dados na matriz de marca de propriedade, mas não pode adicionar novas marcas.</span><span class="sxs-lookup"><span data-stu-id="147a4-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="147a4-138">**HrAddColumnsEx** primeiro chama a função de retorno de chamada, se uma for fornecida, adiciona ou move as colunas especificadas e, finalmente, chama IMAPITable [::](imapitable-setcolumns.md)SetColumns.</span><span class="sxs-lookup"><span data-stu-id="147a4-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="147a4-139">Os parâmetros de entrada _lpAllocateBuffer_ e _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="147a4-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="147a4-140">Os valores exatos dos ponteiros passados para **HrAddColumnsEx** dependem do fato de o chamador ser um aplicativo cliente ou um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="147a4-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="147a4-141">Um cliente passa ponteiros para as funções MAPI com os nomes especificados.</span><span class="sxs-lookup"><span data-stu-id="147a4-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="147a4-142">Um provedor de serviços passa os ponteiros recebidos em sua chamada de inicialização ou recuperados chamando o método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="147a4-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="147a4-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="147a4-143">See also</span></span>



[<span data-ttu-id="147a4-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="147a4-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

