---
title: IMsgServiceAdminDeleteMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.DeleteMsgService
api_type:
- COM
ms.assetid: 3a6b34eb-9d46-488f-8d02-91b27c35de67
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0a3021ed386aa00777694452a755693fc4078093
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767459"
---
# <a name="imsgserviceadmindeletemsgservice"></a><span data-ttu-id="86406-103">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="86406-103">IMsgServiceAdmin::DeleteMsgService</span></span>

  
  
<span data-ttu-id="86406-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86406-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86406-105">Exclui um serviço de mensagem de um perfil.</span><span class="sxs-lookup"><span data-stu-id="86406-105">Deletes a message service from a profile.</span></span>
  
```cpp
HRESULT DeleteMsgService(
  LPMAPIUID lpuid
);
```

## <a name="parameters"></a><span data-ttu-id="86406-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86406-106">Parameters</span></span>

 <span data-ttu-id="86406-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="86406-107">_lpuid_</span></span>
  
> <span data-ttu-id="86406-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="86406-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to delete.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="86406-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="86406-109">Return value</span></span>

<span data-ttu-id="86406-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="86406-110">S_OK</span></span> 
  
> <span data-ttu-id="86406-111">O serviço de mensagem foi excluído.</span><span class="sxs-lookup"><span data-stu-id="86406-111">The message service was deleted.</span></span>
    
<span data-ttu-id="86406-112">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="86406-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="86406-113">**MAPIUID** apontado pela _lpuid_ não corresponde a um serviço de mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="86406-113">The **MAPIUID** pointed to by  _lpuid_ does not match an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="86406-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="86406-114">Remarks</span></span>

<span data-ttu-id="86406-115">O método **IMsgServiceAdmin::DeleteMsgService** exclui um serviço de mensagem de um perfil.</span><span class="sxs-lookup"><span data-stu-id="86406-115">The **IMsgServiceAdmin::DeleteMsgService** method deletes a message service from a profile.</span></span> <span data-ttu-id="86406-116">**DeleteMsgService** remove todas as seções de perfil relacionadas ao serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86406-116">**DeleteMsgService** removes all profile sections related to the message service.</span></span> 
  
 <span data-ttu-id="86406-117">**DeleteMsgService** executa as seguintes etapas para excluir o serviço de mensagem:</span><span class="sxs-lookup"><span data-stu-id="86406-117">**DeleteMsgService** performs the following steps to delete the message service:</span></span> 
  
1. <span data-ttu-id="86406-118">Chama a função de ponto de entrada do serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_DELETE antes que as seções de perfil são removidas.</span><span class="sxs-lookup"><span data-stu-id="86406-118">Calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE before the profile sections are removed.</span></span> <span data-ttu-id="86406-119">Isso permite que o serviço de realizar tarefas específicas do serviço.</span><span class="sxs-lookup"><span data-stu-id="86406-119">This allows the service to perform any service-specific tasks.</span></span> 
    
2. <span data-ttu-id="86406-120">Exclui o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86406-120">Deletes the message service.</span></span>
    
3. <span data-ttu-id="86406-121">Exclui a seção de perfil do serviço na mensagem.</span><span class="sxs-lookup"><span data-stu-id="86406-121">Deletes the message service's profile section.</span></span>
    
<span data-ttu-id="86406-122">Função do ponto de entrada do serviço de mensagem não é chamada novamente depois que o serviço foi excluído.</span><span class="sxs-lookup"><span data-stu-id="86406-122">The message service's entry point function is not called again after the service has been deleted.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="86406-123">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="86406-123">Notes to callers</span></span>

<span data-ttu-id="86406-124">Para recuperar a estrutura **MAPIUID** para o serviço de mensagem excluir, recupere a coluna de propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagem da tabela de serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86406-124">To retrieve the **MAPIUID** structure for the message service to delete, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="86406-125">Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="86406-125">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="86406-126">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="86406-126">MFCMAPI reference</span></span>

<span data-ttu-id="86406-127">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="86406-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="86406-128">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="86406-128">**File**</span></span>|<span data-ttu-id="86406-129">**Function**</span><span class="sxs-lookup"><span data-stu-id="86406-129">**Function**</span></span>|<span data-ttu-id="86406-130">**Comment**</span><span class="sxs-lookup"><span data-stu-id="86406-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86406-131">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="86406-131">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="86406-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="86406-132">CMsgServiceTableDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="86406-133">MFCMAPI usa o método **IMsgServiceAdmin::DeleteMsgService** para excluir o serviço selecionado.</span><span class="sxs-lookup"><span data-stu-id="86406-133">MFCMAPI uses the **IMsgServiceAdmin::DeleteMsgService** method to delete the selected service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86406-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="86406-134">See also</span></span>



[<span data-ttu-id="86406-135">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="86406-135">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="86406-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="86406-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="86406-137">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="86406-137">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

