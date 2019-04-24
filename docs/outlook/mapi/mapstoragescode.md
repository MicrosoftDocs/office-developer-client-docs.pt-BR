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
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357628"
---
# <a name="mapstoragescode"></a><span data-ttu-id="047ff-103">MapStorageSCode</span><span class="sxs-lookup"><span data-stu-id="047ff-103">MapStorageSCode</span></span>

  
  
<span data-ttu-id="047ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="047ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="047ff-105">Mapeia um valor de retorno SCODE de um objeto de armazenamento OLE para um tipo HRESULT.</span><span class="sxs-lookup"><span data-stu-id="047ff-105">Maps an SCODE return value from an OLE storage object to an HRESULT type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="047ff-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="047ff-106">Header file:</span></span>  <br/> |<span data-ttu-id="047ff-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="047ff-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="047ff-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="047ff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="047ff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="047ff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="047ff-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="047ff-110">Called by:</span></span>  <br/> |<span data-ttu-id="047ff-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="047ff-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a><span data-ttu-id="047ff-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="047ff-112">Parameters</span></span>

 <span data-ttu-id="047ff-113">_StgSCode_</span><span class="sxs-lookup"><span data-stu-id="047ff-113">_StgSCode_</span></span>
  
> <span data-ttu-id="047ff-114">no SCODE MAPI valor de retorno de um objeto de armazenamento OLE a ser mapeado para um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="047ff-114">[in] MAPI SCODE return value from an OLE storage object to be mapped to a HRESULT value.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="047ff-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="047ff-115">Return value</span></span>

<span data-ttu-id="047ff-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="047ff-116">S_OK</span></span> 
  
> <span data-ttu-id="047ff-117">A chamada teve êxito e retornou o valor esperado.</span><span class="sxs-lookup"><span data-stu-id="047ff-117">The call succeeded and returned the expected value.</span></span>
    
<span data-ttu-id="047ff-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="047ff-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="047ff-119">A função não pode localizar um valor correspondente.</span><span class="sxs-lookup"><span data-stu-id="047ff-119">The function cannot find a matching value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="047ff-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="047ff-120">Remarks</span></span>

<span data-ttu-id="047ff-121">MAPI fornece a função **MapStorageSCode** para o uso interno de componentes MAPI que baseiam suas implementações de mensagem na DLL de mensagens.</span><span class="sxs-lookup"><span data-stu-id="047ff-121">MAPI provides the **MapStorageSCode** function for the internal use of MAPI components that base their message implementations on the message DLL.</span></span> <span data-ttu-id="047ff-122">Como esses componentes abrem o armazenamento OLE, eles devem ser capazes de mapear valores de erro retornados para problemas com o armazenamento OLE para um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="047ff-122">Because these components open OLE storage themselves, they must be able to map error values returned for problems with OLE storage to an HRESULT value.</span></span> 
  
<span data-ttu-id="047ff-123">Para obter mais informações, consulte [Structured Storage](structured-storage-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="047ff-123">For more information, see [Structured Storage](structured-storage-in-mapi.md).</span></span> 
  

