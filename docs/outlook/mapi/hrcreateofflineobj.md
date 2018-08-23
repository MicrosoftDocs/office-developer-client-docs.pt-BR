---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f86266f192ffb1c86ca48f0fd5f99559737a9e76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576481"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="3852b-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3852b-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="3852b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3852b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3852b-105">Cria um objeto offline MAPI que é usado pelo provedor e repositório para notificar MAPI quando o objeto fica online e offline,</span><span class="sxs-lookup"><span data-stu-id="3852b-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3852b-106">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="3852b-106">Exported by:</span></span>  <br/> |<span data-ttu-id="3852b-107">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="3852b-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="3852b-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3852b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3852b-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="3852b-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="3852b-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3852b-110">Called by:</span></span>  <br/> |<span data-ttu-id="3852b-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="3852b-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="3852b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3852b-112">Parameters</span></span>

<span data-ttu-id="3852b-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3852b-113">_ulFlags_</span></span>
  
> <span data-ttu-id="3852b-114">[in] Ela deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="3852b-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="3852b-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="3852b-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="3852b-116">[in] Um ponteiro para uma estrutura **MAPIOFFLINE_CREATEINFO** que contém as informações necessárias para criar o objeto offline.</span><span class="sxs-lookup"><span data-stu-id="3852b-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="3852b-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="3852b-117">_ppOffline_</span></span>
  
> <span data-ttu-id="3852b-118">[out] Um ponteiro para a interface **IMAPIOfflineMgr** .</span><span class="sxs-lookup"><span data-stu-id="3852b-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3852b-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3852b-119">Return value</span></span>

<span data-ttu-id="3852b-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="3852b-120">None.</span></span>
  
<span data-ttu-id="3852b-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3852b-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="3852b-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3852b-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="3852b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3852b-123">See also</span></span>

- [<span data-ttu-id="3852b-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="3852b-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="3852b-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="3852b-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

