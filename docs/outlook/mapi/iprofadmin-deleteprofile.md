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
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419587"
---
# <a name="iprofadmindeleteprofile"></a><span data-ttu-id="1ce04-103">IProfAdmin::DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="1ce04-103">IProfAdmin::DeleteProfile</span></span>

  
  
<span data-ttu-id="1ce04-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ce04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ce04-105">Exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="1ce04-105">Deletes a profile.</span></span>
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1ce04-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ce04-106">Parameters</span></span>

 <span data-ttu-id="1ce04-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="1ce04-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="1ce04-108">no Um ponteiro para o nome do perfil a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1ce04-108">[in] A pointer to the name of the profile to be deleted.</span></span>
    
 <span data-ttu-id="1ce04-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ce04-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1ce04-110">no Sempre nulo.</span><span class="sxs-lookup"><span data-stu-id="1ce04-110">[in] Always NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ce04-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1ce04-111">Return value</span></span>

<span data-ttu-id="1ce04-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ce04-112">S_OK</span></span> 
  
> <span data-ttu-id="1ce04-113">O perfil foi excluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="1ce04-113">The profile was successfully deleted.</span></span>
    
<span data-ttu-id="1ce04-114">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1ce04-114">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1ce04-115">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="1ce04-115">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ce04-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ce04-116">Remarks</span></span>

<span data-ttu-id="1ce04-117">O método **IProfAdmin::D eleteprofile** exclui um perfil.</span><span class="sxs-lookup"><span data-stu-id="1ce04-117">The **IProfAdmin::DeleteProfile** method deletes a profile.</span></span> <span data-ttu-id="1ce04-118">Se o perfil a ser excluído estiver em uso quando **DeleteProfile** for chamado, **DeleteProfile** retornará S_OK, mas não excluirá o perfil imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1ce04-118">If the profile to delete is in use when **DeleteProfile** is called, **DeleteProfile** returns S_OK but does not delete the profile immediately.</span></span> <span data-ttu-id="1ce04-119">Em vez disso, o **DeleteProfile** marca o perfil para exclusão e o exclui depois que ele não está mais sendo usado, quando todas as sessões ativas terminam.</span><span class="sxs-lookup"><span data-stu-id="1ce04-119">Instead, **DeleteProfile** marks the profile for deletion and deletes it after it is no longer being used, when all of its active sessions have ended.</span></span> 
  
<span data-ttu-id="1ce04-120">A função de ponto de entrada para cada serviço de mensagens no perfil é chamada com o valor MSG_SERVICE_DELETE definido no parâmetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="1ce04-120">The entry point function for each message service in the profile is called with the MSG_SERVICE_DELETE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="1ce04-121">Primeiro, a função exclui o serviço e, em seguida, exclui a seção de perfil do serviço.</span><span class="sxs-lookup"><span data-stu-id="1ce04-121">First, the function deletes the service, and then it deletes the service's profile section.</span></span> <span data-ttu-id="1ce04-122">A função de ponto de entrada do serviço de mensagem não é chamada novamente depois que o serviço é excluído.</span><span class="sxs-lookup"><span data-stu-id="1ce04-122">The message service entry point function is not called again after the service has been deleted.</span></span> 
  
<span data-ttu-id="1ce04-123">Nenhuma senha é necessária para excluir um perfil.</span><span class="sxs-lookup"><span data-stu-id="1ce04-123">No password is required to delete a profile.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ce04-124">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1ce04-124">MFCMAPI reference</span></span>

<span data-ttu-id="1ce04-125">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ce04-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ce04-126">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1ce04-126">**File**</span></span>|<span data-ttu-id="1ce04-127">**Função**</span><span class="sxs-lookup"><span data-stu-id="1ce04-127">**Function**</span></span>|<span data-ttu-id="1ce04-128">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1ce04-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ce04-129">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="1ce04-129">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ce04-130">HrRemoveProfile</span><span class="sxs-lookup"><span data-stu-id="1ce04-130">HrRemoveProfile</span></span>  <br/> |<span data-ttu-id="1ce04-131">MFCMAPI usa o método **IProfAdmin::D eleteprofile** para excluir o perfil selecionado.</span><span class="sxs-lookup"><span data-stu-id="1ce04-131">MFCMAPI uses the **IProfAdmin::DeleteProfile** method to delete the selected profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ce04-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ce04-132">See also</span></span>



[<span data-ttu-id="1ce04-133">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="1ce04-133">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="1ce04-134">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="1ce04-134">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="1ce04-135">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ce04-135">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


[<span data-ttu-id="1ce04-136">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1ce04-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

