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
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299423"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="0d3f6-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="0d3f6-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="0d3f6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d3f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d3f6-105">Determina a página de código para um fluxo TNEF (Transport-neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="0d3f6-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d3f6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0d3f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d3f6-107">TNEF. h</span><span class="sxs-lookup"><span data-stu-id="0d3f6-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="0d3f6-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0d3f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d3f6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d3f6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d3f6-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="0d3f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d3f6-111">Aplicativos cliente e provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="0d3f6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d3f6-112">Parameters</span></span>

 <span data-ttu-id="0d3f6-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="0d3f6-113">_lpStream_</span></span>
  
> <span data-ttu-id="0d3f6-114">no Ponteiro para um objeto de fluxo de armazenamento interface **IStream** de OLE, fornecendo uma fonte para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="0d3f6-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="0d3f6-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="0d3f6-116">bota Ponteiro para a página de código do Stream.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="0d3f6-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="0d3f6-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="0d3f6-118">bota Ponteiro para a página de subcódigo do Stream.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d3f6-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d3f6-119">Return value</span></span>

 <span data-ttu-id="0d3f6-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="0d3f6-120">**S_OK**</span></span>
  
> <span data-ttu-id="0d3f6-121">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="0d3f6-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="0d3f6-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="0d3f6-123">Ocorreu um erro ao ler um atributo no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="0d3f6-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="0d3f6-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="0d3f6-125">O Stream não era um fluxo TNEF ou houve um erro ao ler o atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d3f6-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d3f6-126">Remarks</span></span>

<span data-ttu-id="0d3f6-127">Use a função **GetTnefStreamCodepage** para ler o atributo **ATTOEMCODEPAGE** do fluxo TNEF para determinar a página de código e a página de subcódigo.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="0d3f6-128">Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retornará uma página de código de 437 e uma página de subcódigo 0.</span><span class="sxs-lookup"><span data-stu-id="0d3f6-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d3f6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d3f6-129">See also</span></span>



[<span data-ttu-id="0d3f6-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="0d3f6-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

