---
title: IMsgServiceAdminRenameMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.RenameMsgService
api_type:
- COM
ms.assetid: eba0e7f2-03c1-4713-aa36-3d0b398cd197
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ff748827950c79c3c94e9f70ce8b0bb335884290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767474"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="7cdc0-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="7cdc0-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="7cdc0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cdc0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cdc0-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-105">Deprecated.</span></span> <span data-ttu-id="7cdc0-106">Atribui um novo nome para um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="7cdc0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cdc0-107">Parameters</span></span>

 <span data-ttu-id="7cdc0-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="7cdc0-108">_lpUID_</span></span>
  
> <span data-ttu-id="7cdc0-109">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem renomear.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="7cdc0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7cdc0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="7cdc0-111">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7cdc0-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="7cdc0-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="7cdc0-113">[in] Um ponteiro para o novo nome para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7cdc0-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7cdc0-114">Return value</span></span>

<span data-ttu-id="7cdc0-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="7cdc0-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="7cdc0-116">MAPI não oferece suporte para renomear este serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="7cdc0-117">**RenameMsgService** sempre retorna este valor.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7cdc0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cdc0-118">Remarks</span></span>

<span data-ttu-id="7cdc0-119">Para atribuir um novo nome para um serviço de mensagem, os clientes devem usar a propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7cdc0-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="7cdc0-120">Os nomes dos provedores de serviços em um serviço de mensagem são armazenados em suas propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7cdc0-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7cdc0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cdc0-121">See also</span></span>



[<span data-ttu-id="7cdc0-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7cdc0-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7cdc0-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7cdc0-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

