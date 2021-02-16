---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410354"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="70f48-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="70f48-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="70f48-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f48-105">Modifica a senha de um provedor de serviços sem exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="70f48-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="70f48-106">Opcionalmente, esse método tem suporte em objetos de status implementados por provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="70f48-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="70f48-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70f48-107">Parameters</span></span>

 <span data-ttu-id="70f48-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="70f48-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="70f48-109">[in] Um ponteiro para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="70f48-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="70f48-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="70f48-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="70f48-111">[in] Um ponteiro para a nova senha.</span><span class="sxs-lookup"><span data-stu-id="70f48-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="70f48-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70f48-112">_ulFlags_</span></span>
  
> <span data-ttu-id="70f48-113">[in] Uma máscara de bits de sinalizadores que controla o formato das senhas.</span><span class="sxs-lookup"><span data-stu-id="70f48-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="70f48-114">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="70f48-114">The following flag can be set:</span></span>
    
<span data-ttu-id="70f48-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70f48-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70f48-116">As senhas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="70f48-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="70f48-117">Se o MAPI_UNICODE sinalizador não estiver definido, as senhas estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="70f48-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70f48-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="70f48-118">Return value</span></span>

<span data-ttu-id="70f48-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="70f48-119">S_OK</span></span> 
  
> <span data-ttu-id="70f48-120">A modificação de senha foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="70f48-120">The password modification was successful.</span></span>
    
<span data-ttu-id="70f48-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="70f48-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="70f48-122">A senha antiga apontada por  _lpOldPass_ é inválida.</span><span class="sxs-lookup"><span data-stu-id="70f48-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="70f48-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="70f48-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="70f48-124">O objeto de status não dá suporte a essa operação, conforme indicado pela ausência do sinalizador STATUS_CHANGE_PASSWORD na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto de status.</span><span class="sxs-lookup"><span data-stu-id="70f48-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70f48-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="70f48-125">Remarks</span></span>

<span data-ttu-id="70f48-126">Nem todos os objetos de status suportam o **método IMAPIStatus::ChangePassword.**</span><span class="sxs-lookup"><span data-stu-id="70f48-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="70f48-127">Há suporte apenas para provedores de serviços que exigem que os clientes insiram uma senha.</span><span class="sxs-lookup"><span data-stu-id="70f48-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="70f48-128">Nenhum dos objetos de status que o MAPI implementa suporta a operação de alteração de senha.</span><span class="sxs-lookup"><span data-stu-id="70f48-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="70f48-129">**ChangePassword** modifica uma senha programaticamente, sem interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="70f48-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="70f48-130">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="70f48-130">Notes to implementers</span></span>

<span data-ttu-id="70f48-131">Os provedores de transporte **remoto implementam ChangePassword** conforme especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="70f48-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="70f48-132">Não há considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="70f48-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70f48-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="70f48-133">See also</span></span>



[<span data-ttu-id="70f48-134">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="70f48-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="70f48-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="70f48-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

