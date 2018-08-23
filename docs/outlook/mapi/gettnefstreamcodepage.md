---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d00a2ce3ebec24ca69875bdcb83066d8b891137a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585952"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="c5772-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="c5772-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="c5772-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5772-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5772-105">Determina a página de código para um fluxo de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="c5772-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5772-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c5772-106">Header file:</span></span>  <br/> |<span data-ttu-id="c5772-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="c5772-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="c5772-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c5772-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c5772-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c5772-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c5772-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c5772-110">Called by:</span></span>  <br/> |<span data-ttu-id="c5772-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="c5772-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="c5772-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5772-112">Parameters</span></span>

 <span data-ttu-id="c5772-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="c5772-113">_lpStream_</span></span>
  
> <span data-ttu-id="c5772-114">[in] Ponteiro para um armazenamento stream objeto OLE **IStream** interface, fornecendo uma fonte para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="c5772-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="c5772-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="c5772-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="c5772-116">[out] Ponteiro para a página de código do fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5772-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="c5772-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="c5772-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="c5772-118">[out] Ponteiro para a página subcódigo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="c5772-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c5772-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c5772-119">Return value</span></span>

 <span data-ttu-id="c5772-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="c5772-120">**S_OK**</span></span>
  
> <span data-ttu-id="c5772-121">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="c5772-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="c5772-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="c5772-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="c5772-123">Houve um erro ao ler um atributo no stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="c5772-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="c5772-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="c5772-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="c5772-125">O fluxo não era um stream TNEF ou houve um erro ao ler o atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="c5772-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5772-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5772-126">Remarks</span></span>

<span data-ttu-id="c5772-127">Use a função **GetTnefStreamCodepage** para ler o atributo **attOemCodepage** do stream TNEF para determinar a página de código e a página subcódigo.</span><span class="sxs-lookup"><span data-stu-id="c5772-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="c5772-128">Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retorna uma página de código dos 437 e uma página de subcódigo 0.</span><span class="sxs-lookup"><span data-stu-id="c5772-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5772-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5772-129">See also</span></span>



[<span data-ttu-id="c5772-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="c5772-130">attOemCodepage</span></span>](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

