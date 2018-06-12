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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767171"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="bd605-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="bd605-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="bd605-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd605-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd605-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bd605-105">Deprecated.</span></span> <span data-ttu-id="bd605-106">Retorna os tipos de endereço que podem ser administrados por todos os provedores de transporte na sessão.</span><span class="sxs-lookup"><span data-stu-id="bd605-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="bd605-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="bd605-107">Parameters</span></span>

 <span data-ttu-id="bd605-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd605-108">_ulFlags_</span></span>
  
> <span data-ttu-id="bd605-109">[in] Uma bitmask dos sinalizadores que indica o formato para os tipos de endereço retornado.</span><span class="sxs-lookup"><span data-stu-id="bd605-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="bd605-110">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="bd605-110">The following flag can be set:</span></span>
    
<span data-ttu-id="bd605-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd605-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bd605-112">Os tipos de endereço estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd605-112">The address types are in Unicode format.</span></span> <span data-ttu-id="bd605-113">Se o sinalizador MAPI_UNICODE não estiver definido, os tipos de endereço estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="bd605-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="bd605-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="bd605-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="bd605-115">[out] Um ponteiro para uma contagem de tipos de endereço apontado pelo parâmetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="bd605-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="bd605-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="bd605-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="bd605-117">[out] Um ponteiro para uma matriz de ponteiros para tipos de endereço.</span><span class="sxs-lookup"><span data-stu-id="bd605-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd605-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd605-118">Return value</span></span>

<span data-ttu-id="bd605-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd605-119">S_OK</span></span> 
  
> <span data-ttu-id="bd605-120">Os tipos de endereço foram recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="bd605-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd605-121">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bd605-121">Remarks</span></span>

<span data-ttu-id="bd605-122">O método **IMAPISession::EnumAdrTypes** retorna uma lista dos tipos de endereço que podem ser administrados por todos os provedores de transporte ativa na sessão.</span><span class="sxs-lookup"><span data-stu-id="bd605-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="bd605-123">Os tipos de endereço para provedores de transporte que não são carregadas no momento não são incluídos na lista.</span><span class="sxs-lookup"><span data-stu-id="bd605-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="bd605-124">Provedores de transporte Registre-se para lidar com um ou mais tipos de endereço ao seu método de [IXPLogon::AddressTypes](ixplogon-addresstypes.md) chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd605-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bd605-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="bd605-125">Notes to callers</span></span>

<span data-ttu-id="bd605-126">Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de cadeia de caracteres apontada pelo parâmetro _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="bd605-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd605-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd605-127">See also</span></span>



[<span data-ttu-id="bd605-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="bd605-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="bd605-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bd605-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bd605-130">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd605-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

