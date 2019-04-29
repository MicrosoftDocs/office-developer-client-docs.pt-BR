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
ms.openlocfilehash: 2f0f1fb94ea36512bbc40df8a4877e89d2613a25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422100"
---
# <a name="imsgserviceadminrenamemsgservice"></a><span data-ttu-id="4972e-103">IMsgServiceAdmin::RenameMsgService</span><span class="sxs-lookup"><span data-stu-id="4972e-103">IMsgServiceAdmin::RenameMsgService</span></span>

  
  
<span data-ttu-id="4972e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4972e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4972e-105">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4972e-105">Deprecated.</span></span> <span data-ttu-id="4972e-106">Atribui um novo nome a um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4972e-106">Assigns a new name to a message service.</span></span> 
  
```cpp
HRESULT RenameMsgService(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPSTR lpszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="4972e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4972e-107">Parameters</span></span>

 <span data-ttu-id="4972e-108">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="4972e-108">_lpUID_</span></span>
  
> <span data-ttu-id="4972e-109">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="4972e-109">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to rename.</span></span> 
    
 <span data-ttu-id="4972e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4972e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="4972e-111">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4972e-111">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4972e-112">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="4972e-112">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="4972e-113">no Um ponteiro para o novo nome do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4972e-113">[in] A pointer to the new name for the message service.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4972e-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4972e-114">Return value</span></span>

<span data-ttu-id="4972e-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4972e-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4972e-116">O MAPI não dá suporte à renomeação deste serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4972e-116">MAPI does not support renaming this message service.</span></span> <span data-ttu-id="4972e-117">**RenameMsgService** sempre retorna esse valor.</span><span class="sxs-lookup"><span data-stu-id="4972e-117">**RenameMsgService** always returns this value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4972e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4972e-118">Remarks</span></span>

<span data-ttu-id="4972e-119">Para atribuir um novo nome a um serviço de mensagens, os clientes devem usar a propriedade **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="4972e-119">To assign a new name to a message service, clients should use the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property of the message service.</span></span> <span data-ttu-id="4972e-120">Os nomes de provedores de serviço em um serviço de mensagens são armazenados em suas propriedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4972e-120">The names of service providers in a message service are stored in their **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4972e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4972e-121">See also</span></span>



[<span data-ttu-id="4972e-122">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="4972e-122">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="4972e-123">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4972e-123">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

