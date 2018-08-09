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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767208"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="91052-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="91052-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="91052-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91052-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91052-105">Modifica a senha de um provedor de serviços sem exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="91052-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="91052-106">Opcionalmente, esse método é suportado nos objetos de status que implementam provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="91052-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="91052-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91052-107">Parameters</span></span>

 <span data-ttu-id="91052-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="91052-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="91052-109">[in] Um ponteiro para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="91052-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="91052-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="91052-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="91052-111">[in] Um ponteiro para a nova senha.</span><span class="sxs-lookup"><span data-stu-id="91052-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="91052-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91052-112">_ulFlags_</span></span>
  
> <span data-ttu-id="91052-113">[in] Uma bitmask dos sinalizadores que controla o formato das senhas.</span><span class="sxs-lookup"><span data-stu-id="91052-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="91052-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="91052-114">The following flag can be set:</span></span>
    
<span data-ttu-id="91052-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91052-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91052-116">As senhas são no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="91052-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="91052-117">Se o sinalizador MAPI_UNICODE não estiver definido, as senhas são no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="91052-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91052-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="91052-118">Return value</span></span>

<span data-ttu-id="91052-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="91052-119">S_OK</span></span> 
  
> <span data-ttu-id="91052-120">A modificação de senha foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="91052-120">The password modification was successful.</span></span>
    
<span data-ttu-id="91052-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="91052-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="91052-122">A senha antiga apontada pela _lpOldPass_ é inválida.</span><span class="sxs-lookup"><span data-stu-id="91052-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="91052-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="91052-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="91052-124">O objeto status não suporta essa operação, conforme indicado pela ausência do sinalizador STATUS_CHANGE_PASSWORD na propriedade de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.</span><span class="sxs-lookup"><span data-stu-id="91052-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91052-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="91052-125">Remarks</span></span>

<span data-ttu-id="91052-126">Nem todos os objetos de status suportam ao método **IMAPIStatus:: ChangePassword** .</span><span class="sxs-lookup"><span data-stu-id="91052-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="91052-127">Ele é suportado somente por provedores de serviços que exigem que os clientes a digitar uma senha.</span><span class="sxs-lookup"><span data-stu-id="91052-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="91052-128">Nenhum dos objetos status que implementa MAPI suporte à operação de alteração de senha.</span><span class="sxs-lookup"><span data-stu-id="91052-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="91052-129">**ChangePassword** modifica uma senha programaticamente, sem interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="91052-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="91052-130">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="91052-130">Notes to implementers</span></span>

<span data-ttu-id="91052-131">Provedores de transporte remoto implementam **ChangePassword** conforme especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="91052-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="91052-132">Não há nenhuma considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="91052-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91052-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="91052-133">See also</span></span>



[<span data-ttu-id="91052-134">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="91052-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="91052-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="91052-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

