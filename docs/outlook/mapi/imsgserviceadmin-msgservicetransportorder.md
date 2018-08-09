---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767487"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="5a0d5-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="5a0d5-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="5a0d5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a0d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a0d5-105">Define a ordem na qual transporte provedores são chamados para entregar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="5a0d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a0d5-106">Parameters</span></span>

 <span data-ttu-id="5a0d5-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="5a0d5-107">_cUID_</span></span>
  
> <span data-ttu-id="5a0d5-108">[in] A contagem de identificadores exclusivos no parâmetro _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="5a0d5-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="5a0d5-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="5a0d5-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="5a0d5-110">[in] Um ponteiro para uma matriz de identificadores exclusivos que representam os provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="5a0d5-111">A matriz contém um identificador para cada provedor de transporte configurada no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="5a0d5-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a0d5-112">_ulFlags_</span></span>
  
> <span data-ttu-id="5a0d5-113">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a0d5-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5a0d5-114">Return value</span></span>

<span data-ttu-id="5a0d5-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a0d5-115">S_OK</span></span> 
  
> <span data-ttu-id="5a0d5-116">A ordem de transporte foi definida com êxito.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="5a0d5-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5a0d5-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5a0d5-118">O valor no parâmetro _cUID_ difere do número de provedores de transporte realmente no perfil.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="5a0d5-119">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5a0d5-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5a0d5-120">Uma ou mais das estruturas [MAPIUID](mapiuid.md) passadas no parâmetro _lpUIDList_ não fazem referência a um provedor de transporte no momento no perfil.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a0d5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a0d5-121">Remarks</span></span>

<span data-ttu-id="5a0d5-122">O método **IMsgServiceAdmin::MsgServiceTransportOrder** define a ordem de entrega de provedores de transporte em um perfil.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="5a0d5-123">O parâmetro _lpUIDList_ deve conter uma lista classificada dos identificadores de entrada do provedor de transporte obtidos da propriedade **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) da tabela retornada do [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) método.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="5a0d5-124">Um aplicativo cliente deve passar a lista completa em _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="5a0d5-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="5a0d5-125">Substituições **SetTransportOrder** transportam preferências de provedor, como o sinalizador STATUS_XP_PREFER_LAST definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5a0d5-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5a0d5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a0d5-126">See also</span></span>



[<span data-ttu-id="5a0d5-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5a0d5-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5a0d5-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a0d5-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

