---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab892513348541ec9de3c071a12268afa9337465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768039"
---
# <a name="mapstoragescode"></a><span data-ttu-id="51b77-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="51b77-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="51b77-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51b77-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51b77-105">Mapas de um SCODE retornam o valor de um objeto de armazenamento OLE para um tipo HRESULT.</span><span class="sxs-lookup"><span data-stu-id="51b77-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51b77-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="51b77-106">Header file:</span></span>  <br/> |<span data-ttu-id="51b77-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="51b77-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="51b77-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="51b77-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="51b77-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="51b77-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="51b77-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="51b77-110">Called by:</span></span>  <br/> |<span data-ttu-id="51b77-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="51b77-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="51b77-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51b77-112">Parameters</span></span>

 <span data-ttu-id="51b77-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="51b77-113">_StgSCode_</span></span>
  
> <span data-ttu-id="51b77-114">[in] Valor de retorno de MAPI SCODE de um objeto de armazenamento OLE sejam mapeados para um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="51b77-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51b77-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="51b77-115">Return value</span></span>

<span data-ttu-id="51b77-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="51b77-116">S_OK</span></span> 
  
> <span data-ttu-id="51b77-117">A chamada foi bem-sucedida e retornou o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="51b77-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="51b77-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="51b77-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="51b77-119">A função não puder localizar um valor coincidente.</span><span class="sxs-lookup"><span data-stu-id="51b77-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51b77-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="51b77-120">Remarks</span></span>

<span data-ttu-id="51b77-121">MAPI fornece a função **MapStorageSCode** para uso interno de componentes MAPI que basear suas implementações de mensagem na mensagem de DLL.</span><span class="sxs-lookup"><span data-stu-id="51b77-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="51b77-122">Porque esses componentes abrir o armazenamento OLE sozinhos, ele devem ser capaz de mapear os valores de erro retornados para problemas com o armazenamento OLE para um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="51b77-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="51b77-123">Para obter mais informações, consulte [Armazenamento estruturado](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="51b77-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

