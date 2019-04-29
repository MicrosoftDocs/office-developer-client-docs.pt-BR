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
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422758"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="11e31-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="11e31-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="11e31-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11e31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11e31-105">Retorna um ponteiro que fornece acesso a um objeto de administração de provedor.</span><span class="sxs-lookup"><span data-stu-id="11e31-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="11e31-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e31-106">Parameters</span></span>

 <span data-ttu-id="11e31-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="11e31-107">_lpUID_</span></span>
  
> <span data-ttu-id="11e31-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagens a ser administrado.</span><span class="sxs-lookup"><span data-stu-id="11e31-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="11e31-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11e31-109">_ulFlags_</span></span>
  
> <span data-ttu-id="11e31-110">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="11e31-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="11e31-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="11e31-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="11e31-112">bota Um ponteiro para um ponteiro para um objeto de administração de provedor.</span><span class="sxs-lookup"><span data-stu-id="11e31-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11e31-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="11e31-113">Return value</span></span>

<span data-ttu-id="11e31-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="11e31-114">S_OK</span></span> 
  
> <span data-ttu-id="11e31-115">O objeto de administração de provedor foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="11e31-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="11e31-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="11e31-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="11e31-117">O **MAPIUID** apontado por _lpUID_ não existe.</span><span class="sxs-lookup"><span data-stu-id="11e31-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="11e31-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="11e31-118">Remarks</span></span>

<span data-ttu-id="11e31-119">O método **IMsgServiceAdmin:: AdminProviders** fornece acesso a um objeto de administração de provedor.</span><span class="sxs-lookup"><span data-stu-id="11e31-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="11e31-120">Uma administração de provedor é um objeto que dá suporte à interface [IProviderAdmin](iprovideradminiunknown.md) e permite que os clientes façam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="11e31-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="11e31-121">Adicionar provedores de serviços a um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11e31-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="11e31-122">Excluir provedores de serviços de um serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11e31-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="11e31-123">Abrir seções de perfil.</span><span class="sxs-lookup"><span data-stu-id="11e31-123">Open profile sections.</span></span>
    
- <span data-ttu-id="11e31-124">Acessar a tabela do provedor de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11e31-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="11e31-125">Os tipos de alterações que podem ser realmente feitas em um serviço de mensagens enquanto o perfil está em uso dependem do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11e31-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="11e31-126">No enTanto, a maioria dos serviços de mensagem não oferece suporte a alterações como adicionar e excluir provedores enquanto o perfil está em uso.</span><span class="sxs-lookup"><span data-stu-id="11e31-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="11e31-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="11e31-127">Notes to callers</span></span>

<span data-ttu-id="11e31-128">Para recuperar a estrutura **MAPIUID** do serviço de mensagens a administrar, recupere a coluna de propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagens na tabela de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="11e31-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="11e31-129">Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="11e31-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="11e31-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="11e31-130">MFCMAPI reference</span></span>

<span data-ttu-id="11e31-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="11e31-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="11e31-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="11e31-132">**File**</span></span>|<span data-ttu-id="11e31-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="11e31-133">**Function**</span></span>|<span data-ttu-id="11e31-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="11e31-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="11e31-135">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="11e31-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="11e31-136">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="11e31-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="11e31-137">MFCMAPI usa o método **IMsgServiceAdmin:: AdminProviders** para abrir um objeto de administração de provedor para um serviço.</span><span class="sxs-lookup"><span data-stu-id="11e31-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11e31-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="11e31-138">See also</span></span>



[<span data-ttu-id="11e31-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11e31-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="11e31-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="11e31-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="11e31-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11e31-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="11e31-142">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="11e31-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

