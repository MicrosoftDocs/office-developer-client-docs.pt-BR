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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a6eba20fb346f53052808abf8fcae8993d423d34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589557"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="53ded-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="53ded-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="53ded-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ded-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ded-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="53ded-105">Deprecated.</span></span> <span data-ttu-id="53ded-106">Atribui um novo nome para um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="53ded-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="53ded-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53ded-107">Parameters</span></span>

 <span data-ttu-id="53ded-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="53ded-108">_lpUID_</span></span>
  
> <span data-ttu-id="53ded-109">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem renomear.</span><span class="sxs-lookup"><span data-stu-id="53ded-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="53ded-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53ded-110">_ulFlags_</span></span>
  
> <span data-ttu-id="53ded-111">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="53ded-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="53ded-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="53ded-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="53ded-113">[in] Um ponteiro para o novo nome para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="53ded-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53ded-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="53ded-114">Return value</span></span>

<span data-ttu-id="53ded-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="53ded-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="53ded-116">MAPI não oferece suporte para renomear este serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="53ded-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="53ded-117">**RenameMsgService** sempre retorna este valor.</span><span class="sxs-lookup"><span data-stu-id="53ded-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53ded-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="53ded-118">Remarks</span></span>

<span data-ttu-id="53ded-119">Para atribuir um novo nome para um serviço de mensagem, os clientes devem usar a propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="53ded-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="53ded-120">Os nomes dos provedores de serviços em um serviço de mensagem são armazenados em suas propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53ded-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53ded-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="53ded-121">See also</span></span>



[<span data-ttu-id="53ded-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="53ded-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="53ded-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53ded-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

