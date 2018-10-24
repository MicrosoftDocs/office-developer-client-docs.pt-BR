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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570790"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="532d6-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="532d6-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="532d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="532d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="532d6-105">Define a ordem na qual transporte provedores são chamados para entregar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="532d6-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="532d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="532d6-106">Parameters</span></span>

 <span data-ttu-id="532d6-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="532d6-107">_cUID_</span></span>
  
> <span data-ttu-id="532d6-108">[in] A contagem de identificadores exclusivos no parâmetro _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="532d6-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="532d6-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="532d6-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="532d6-110">[in] Um ponteiro para uma matriz de identificadores exclusivos que representam os provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="532d6-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="532d6-111">A matriz contém um identificador para cada provedor de transporte configurada no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="532d6-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="532d6-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="532d6-112">_ulFlags_</span></span>
  
> <span data-ttu-id="532d6-113">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="532d6-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="532d6-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="532d6-114">Return value</span></span>

<span data-ttu-id="532d6-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="532d6-115">S_OK</span></span> 
  
> <span data-ttu-id="532d6-116">A ordem de transporte foi definida com êxito.</span><span class="sxs-lookup"><span data-stu-id="532d6-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="532d6-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="532d6-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="532d6-118">O valor no parâmetro _cUID_ difere do número de provedores de transporte realmente no perfil.</span><span class="sxs-lookup"><span data-stu-id="532d6-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="532d6-119">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="532d6-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="532d6-120">Uma ou mais das estruturas [MAPIUID](mapiuid.md) passadas no parâmetro _lpUIDList_ não fazem referência a um provedor de transporte no momento no perfil.</span><span class="sxs-lookup"><span data-stu-id="532d6-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="532d6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="532d6-121">Remarks</span></span>

<span data-ttu-id="532d6-122">O método **IMsgServiceAdmin::MsgServiceTransportOrder** define a ordem de entrega de provedores de transporte em um perfil.</span><span class="sxs-lookup"><span data-stu-id="532d6-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="532d6-123">O parâmetro _lpUIDList_ deve conter uma lista classificada dos identificadores de entrada do provedor de transporte obtidos da propriedade **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) da tabela retornada do [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) método.</span><span class="sxs-lookup"><span data-stu-id="532d6-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="532d6-124">Um aplicativo cliente deve passar a lista completa em _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="532d6-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="532d6-125">Substituições **SetTransportOrder** transportam preferências de provedor, como o sinalizador STATUS_XP_PREFER_LAST definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="532d6-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="532d6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="532d6-126">See also</span></span>



[<span data-ttu-id="532d6-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="532d6-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="532d6-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="532d6-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

