---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767636"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="e90eb-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="e90eb-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="e90eb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e90eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e90eb-105">Exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="e90eb-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e90eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e90eb-106">Parameters</span></span>

 <span data-ttu-id="e90eb-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="e90eb-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="e90eb-108">[in] Um ponteiro para o nome do perfil a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e90eb-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="e90eb-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e90eb-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e90eb-110">[in] Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="e90eb-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e90eb-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e90eb-111">Return value</span></span>

<span data-ttu-id="e90eb-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="e90eb-112">S_OK</span></span> 
  
> <span data-ttu-id="e90eb-113">O perfil foi excluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="e90eb-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="e90eb-114">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e90eb-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e90eb-115">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="e90eb-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e90eb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e90eb-116">Remarks</span></span>

<span data-ttu-id="e90eb-117">O método **IProfAdmin::DeleteProfile** exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="e90eb-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="e90eb-118">Se o perfil para excluir estiver em uso quando **DeleteProfile** é chamado, **DeleteProfile** Retorna S_OK, mas não exclui o perfil imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e90eb-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="e90eb-119">Em vez disso, o **DeleteProfile** marca o perfil para exclusão e exclui-la depois que ele não é mais sendo usado, quando todas as suas sessões ativas tiverem terminado.</span><span class="sxs-lookup"><span data-stu-id="e90eb-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="e90eb-120">A função do ponto de entrada para cada serviço de mensagem no perfil é chamada com o valor MSG_SERVICE_DELETE definido no parâmetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="e90eb-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="e90eb-121">Primeiro, a função exclui o serviço e, em seguida, ele exclui a seção de perfil do serviço.</span><span class="sxs-lookup"><span data-stu-id="e90eb-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="e90eb-122">A função de ponto de entrada de serviço de mensagem não é chamada novamente depois que o serviço foi excluído.</span><span class="sxs-lookup"><span data-stu-id="e90eb-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="e90eb-123">Nenhuma senha é necessária para excluir um perfil.</span><span class="sxs-lookup"><span data-stu-id="e90eb-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e90eb-124">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e90eb-124">MFCMAPI reference</span></span>

<span data-ttu-id="e90eb-125">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e90eb-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e90eb-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e90eb-126">**File**</span></span>|<span data-ttu-id="e90eb-127">**Function**</span><span class="sxs-lookup"><span data-stu-id="e90eb-127">**Function**</span></span>|<span data-ttu-id="e90eb-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e90eb-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e90eb-129">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="e90eb-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="e90eb-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="e90eb-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="e90eb-131">MFCMAPI usa o método **IProfAdmin::DeleteProfile** para excluir o perfil selecionado.</span><span class="sxs-lookup"><span data-stu-id="e90eb-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e90eb-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e90eb-132">See also</span></span>



[<span data-ttu-id="e90eb-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="e90eb-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="e90eb-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="e90eb-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="e90eb-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e90eb-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="e90eb-136">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e90eb-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

