---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c4859fa4f8f55af7913c884e25c96727c063ba79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766657"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="2348e-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="2348e-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="2348e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2348e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2348e-105">Determina a página de código para um fluxo de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="2348e-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2348e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2348e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2348e-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="2348e-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="2348e-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="2348e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2348e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2348e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2348e-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="2348e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2348e-111">Provedores de serviços e aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="2348e-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="2348e-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2348e-112">Parameters</span></span>

 <span data-ttu-id="2348e-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="2348e-113">_lpStream_</span></span>
  
> <span data-ttu-id="2348e-114">[in] Ponteiro para um armazenamento stream objeto OLE **IStream** interface, fornecendo uma fonte para uma mensagem de fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="2348e-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="2348e-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="2348e-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="2348e-116">[out] Ponteiro para a página de código do fluxo.</span><span class="sxs-lookup"><span data-stu-id="2348e-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="2348e-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="2348e-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="2348e-118">[out] Ponteiro para a página subcódigo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="2348e-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2348e-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2348e-119">Return value</span></span>

 <span data-ttu-id="2348e-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="2348e-120">**S_OK**</span></span>
  
> <span data-ttu-id="2348e-121">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="2348e-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="2348e-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="2348e-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="2348e-123">Houve um erro ao ler um atributo no stream TNEF.</span><span class="sxs-lookup"><span data-stu-id="2348e-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="2348e-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="2348e-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="2348e-125">O fluxo não era um stream TNEF ou houve um erro ao ler o atributo attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="2348e-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2348e-126">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2348e-126">Remarks</span></span>

<span data-ttu-id="2348e-127">Use a função **GetTnefStreamCodepage** para ler o atributo **attOemCodepage** do stream TNEF para determinar a página de código e a página subcódigo.</span><span class="sxs-lookup"><span data-stu-id="2348e-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="2348e-128">Se **attOemCodepage** não for encontrado, **GetTnefStreamCodepage** retorna uma página de código dos 437 e uma página de subcódigo 0.</span><span class="sxs-lookup"><span data-stu-id="2348e-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2348e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2348e-129">See also</span></span>



[<span data-ttu-id="2348e-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="2348e-130">attOemCodepage</span></span>](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

