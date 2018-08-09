---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767466"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="63cf1-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="63cf1-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="63cf1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63cf1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63cf1-105">Retorna um ponteiro que fornece acesso a um objeto de administração do provedor.</span><span class="sxs-lookup"><span data-stu-id="63cf1-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="63cf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63cf1-106">Parameters</span></span>

 <span data-ttu-id="63cf1-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="63cf1-107">_lpUID_</span></span>
  
> <span data-ttu-id="63cf1-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem a serem administrados.</span><span class="sxs-lookup"><span data-stu-id="63cf1-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="63cf1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63cf1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="63cf1-110">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="63cf1-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="63cf1-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="63cf1-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="63cf1-112">[out] Um ponteiro para um ponteiro para um objeto de administração do provedor.</span><span class="sxs-lookup"><span data-stu-id="63cf1-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63cf1-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="63cf1-113">Return value</span></span>

<span data-ttu-id="63cf1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="63cf1-114">S_OK</span></span> 
  
> <span data-ttu-id="63cf1-115">O objeto de administração do provedor foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="63cf1-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="63cf1-116">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="63cf1-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="63cf1-117">**MAPIUID** apontado pela _lpUID_ não existe.</span><span class="sxs-lookup"><span data-stu-id="63cf1-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="63cf1-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="63cf1-118">Remarks</span></span>

<span data-ttu-id="63cf1-119">O método **IMsgServiceAdmin::AdminProviders** fornece acesso a um objeto de administração do provedor.</span><span class="sxs-lookup"><span data-stu-id="63cf1-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="63cf1-120">A administração de um provedor é um objeto que dá suporte à interface [IProviderAdmin](iprovideradminiunknown.md) e permite que os clientes façam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="63cf1-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="63cf1-121">Adicione provedores de serviço para um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63cf1-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="63cf1-122">Exclua provedores de serviço de um serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63cf1-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="63cf1-123">Abrir seções de perfil.</span><span class="sxs-lookup"><span data-stu-id="63cf1-123">Open profile sections.</span></span>
    
- <span data-ttu-id="63cf1-124">Acesse a tabela de provedor de serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63cf1-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="63cf1-125">Os tipos de alterações que realmente podem ser feitas para um serviço de mensagem enquanto o perfil estiver em uso dependem do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63cf1-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="63cf1-126">No entanto, a maioria dos serviços de mensagem não suportam alterações como adicionar e excluir provedores enquanto o perfil estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="63cf1-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="63cf1-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="63cf1-127">Notes to callers</span></span>

<span data-ttu-id="63cf1-128">Para recuperar a estrutura **MAPIUID** para administrar o serviço de mensagem, recupere a coluna de propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagem da tabela de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="63cf1-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="63cf1-129">Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="63cf1-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="63cf1-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="63cf1-130">MFCMAPI reference</span></span>

<span data-ttu-id="63cf1-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="63cf1-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="63cf1-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="63cf1-132">**File**</span></span>|<span data-ttu-id="63cf1-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="63cf1-133">**Function**</span></span>|<span data-ttu-id="63cf1-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="63cf1-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63cf1-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="63cf1-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="63cf1-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="63cf1-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="63cf1-137">MFCMAPI usa o método **IMsgServiceAdmin::AdminProviders** para abrir um objeto de administração do provedor de um serviço.</span><span class="sxs-lookup"><span data-stu-id="63cf1-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63cf1-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="63cf1-138">See also</span></span>



[<span data-ttu-id="63cf1-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63cf1-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="63cf1-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="63cf1-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="63cf1-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="63cf1-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="63cf1-142">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="63cf1-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

