---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439286"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="dbea7-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="dbea7-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="dbea7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbea7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbea7-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="dbea7-105">Deprecated.</span></span> <span data-ttu-id="dbea7-106">Retorna os tipos de endereço que podem ser tratados por todos os provedores de transporte na sessão.</span><span class="sxs-lookup"><span data-stu-id="dbea7-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="dbea7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbea7-107">Parameters</span></span>

 <span data-ttu-id="dbea7-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dbea7-108">_ulFlags_</span></span>
  
> <span data-ttu-id="dbea7-109">no Uma bitmask de sinalizadores que indica o formato dos tipos de endereço retornados.</span><span class="sxs-lookup"><span data-stu-id="dbea7-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="dbea7-110">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="dbea7-110">The following flag can be set:</span></span>
    
<span data-ttu-id="dbea7-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dbea7-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dbea7-112">Os tipos de endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="dbea7-112">The address types are in Unicode format.</span></span> <span data-ttu-id="dbea7-113">Se o sinalizador MAPI_UNICODE não estiver definido, os tipos de endereço estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="dbea7-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="dbea7-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="dbea7-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="dbea7-115">bota Um ponteiro para uma contagem de tipos de endereço apontados pelo parâmetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="dbea7-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="dbea7-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="dbea7-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="dbea7-117">bota Um ponteiro para uma matriz de ponteiros para tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="dbea7-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dbea7-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dbea7-118">Return value</span></span>

<span data-ttu-id="dbea7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbea7-119">S_OK</span></span> 
  
> <span data-ttu-id="dbea7-120">Os tipos de endereço foram recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="dbea7-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbea7-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbea7-121">Remarks</span></span>

<span data-ttu-id="dbea7-122">O método **IMAPISession:: EnumAdrTypes** retorna uma lista dos tipos de endereço que podem ser tratados por todos os provedores de transporte ativos na sessão.</span><span class="sxs-lookup"><span data-stu-id="dbea7-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="dbea7-123">Os tipos de endereço para provedores de transporte que não estão carregados atualmente não estão incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="dbea7-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="dbea7-124">Provedores de transporte Registre-se para lidar com um ou mais tipos de endereço quando o MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="dbea7-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dbea7-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="dbea7-125">Notes to callers</span></span>

<span data-ttu-id="dbea7-126">Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de cadeia de caracteres apontada pelo parâmetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="dbea7-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbea7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbea7-127">See also</span></span>



[<span data-ttu-id="dbea7-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="dbea7-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="dbea7-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dbea7-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dbea7-130">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbea7-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

