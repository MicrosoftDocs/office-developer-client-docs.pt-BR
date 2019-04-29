---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405902"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="d548c-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d548c-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="d548c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d548c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d548c-105">Retorna um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações nos serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d548c-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="d548c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d548c-106">Parameters</span></span>

 <span data-ttu-id="d548c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d548c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d548c-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d548c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d548c-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="d548c-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="d548c-110">bota Um ponteiro para um ponteiro para um objeto de administração de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d548c-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d548c-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d548c-111">Return value</span></span>

<span data-ttu-id="d548c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="d548c-112">S_OK</span></span> 
  
> <span data-ttu-id="d548c-113">Um ponteiro para um objeto de administração do serviço de mensagens foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d548c-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="d548c-114">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="d548c-114">Notes to callers</span></span>

<span data-ttu-id="d548c-115">O método **IMAPISession:: adminservices** cria um objeto de administração de serviço de mensagens, um objeto que dá suporte à interface **IMsgServiceAdmin** e retorna um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="d548c-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="d548c-116">Usando esse ponteiro, você pode chamar os métodos **IMsgServiceAdmin** para alterar qualquer um dos serviços de mensagens no perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="d548c-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="d548c-117">Lembre-se de que essas alterações não terão efeito até a próxima sessão; a sessão atual não é afetada.</span><span class="sxs-lookup"><span data-stu-id="d548c-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d548c-118">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d548c-118">MFCMAPI reference</span></span>

<span data-ttu-id="d548c-119">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d548c-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d548c-120">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d548c-120">**File**</span></span>|<span data-ttu-id="d548c-121">**Função**</span><span class="sxs-lookup"><span data-stu-id="d548c-121">**Function**</span></span>|<span data-ttu-id="d548c-122">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="d548c-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d548c-123">MAPIStoreFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="d548c-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d548c-124">GetServername</span><span class="sxs-lookup"><span data-stu-id="d548c-124">GetServerName</span></span>  <br/> |<span data-ttu-id="d548c-125">MFCMAPI usa o método **IMAPISession:: adminservices** para acessar o perfil para ler o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d548c-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d548c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d548c-126">See also</span></span>



[<span data-ttu-id="d548c-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d548c-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="d548c-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="d548c-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="d548c-129">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d548c-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d548c-130">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d548c-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

