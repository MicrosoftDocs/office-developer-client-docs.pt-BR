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
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420091"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="ca21b-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="ca21b-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="ca21b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca21b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca21b-105">Define a ordem na qual os provedores de transporte são chamados para entregar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ca21b-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="ca21b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca21b-106">Parameters</span></span>

 <span data-ttu-id="ca21b-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="ca21b-107">_cUID_</span></span>
  
> <span data-ttu-id="ca21b-108">[in] A contagem de identificadores exclusivos no _parâmetro lpUIDList._</span><span class="sxs-lookup"><span data-stu-id="ca21b-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="ca21b-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="ca21b-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="ca21b-110">[in] Um ponteiro para uma matriz de identificadores exclusivos que representam provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="ca21b-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="ca21b-111">A matriz contém um identificador para cada provedor de transporte configurado no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="ca21b-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="ca21b-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca21b-112">_ulFlags_</span></span>
  
> <span data-ttu-id="ca21b-113">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca21b-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca21b-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca21b-114">Return value</span></span>

<span data-ttu-id="ca21b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca21b-115">S_OK</span></span> 
  
> <span data-ttu-id="ca21b-116">O pedido de transporte foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="ca21b-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="ca21b-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ca21b-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ca21b-118">O valor no parâmetro  _cUID_ difere do número de provedores de transporte no perfil.</span><span class="sxs-lookup"><span data-stu-id="ca21b-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="ca21b-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ca21b-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ca21b-120">Uma ou mais das estruturas [MAPIUID](mapiuid.md) passadas no parâmetro  _lpUIDList_ não se referem a um provedor de transporte atualmente no perfil.</span><span class="sxs-lookup"><span data-stu-id="ca21b-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca21b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca21b-121">Remarks</span></span>

<span data-ttu-id="ca21b-122">O **método IMsgServiceAdmin::MsgServiceTransportOrder** define a ordem de entrega dos provedores de transporte em um perfil.</span><span class="sxs-lookup"><span data-stu-id="ca21b-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="ca21b-123">O _parâmetro lpUIDList_ deve conter uma lista ordenada de identificadores de entrada de provedor de transporte obtidos da propriedade **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) da tabela retornada do método [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="ca21b-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="ca21b-124">Um aplicativo cliente deve passar a lista completa em  _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="ca21b-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="ca21b-125">**SetTransportOrder** substitui as preferências do provedor de transporte, como o sinalizador STATUS_XP_PREFER_LAST definido na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca21b-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca21b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca21b-126">See also</span></span>



[<span data-ttu-id="ca21b-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ca21b-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ca21b-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca21b-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

