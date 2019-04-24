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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328277"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="84ab9-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="84ab9-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="84ab9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84ab9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84ab9-105">Modifica a senha de um provedor de serviços sem exibir uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="84ab9-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="84ab9-106">Opcionalmente, este método é compatível com objetos de status que os provedores de serviços implementam.</span><span class="sxs-lookup"><span data-stu-id="84ab9-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="84ab9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84ab9-107">Parameters</span></span>

 <span data-ttu-id="84ab9-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="84ab9-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="84ab9-109">no Um ponteiro para a senha antiga.</span><span class="sxs-lookup"><span data-stu-id="84ab9-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="84ab9-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="84ab9-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="84ab9-111">no Um ponteiro para a nova senha.</span><span class="sxs-lookup"><span data-stu-id="84ab9-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="84ab9-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84ab9-112">_ulFlags_</span></span>
  
> <span data-ttu-id="84ab9-113">no Uma bitmask de sinalizadores que controla o formato das senhas.</span><span class="sxs-lookup"><span data-stu-id="84ab9-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="84ab9-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="84ab9-114">The following flag can be set:</span></span>
    
<span data-ttu-id="84ab9-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="84ab9-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="84ab9-116">As senhas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="84ab9-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="84ab9-117">Se o sinalizador MAPI_UNICODE não estiver definido, as senhas estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="84ab9-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84ab9-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="84ab9-118">Return value</span></span>

<span data-ttu-id="84ab9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="84ab9-119">S_OK</span></span> 
  
> <span data-ttu-id="84ab9-120">A modificação de senha foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="84ab9-120">The password modification was successful.</span></span>
    
<span data-ttu-id="84ab9-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="84ab9-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="84ab9-122">A senha antiga indicada por _lpOldPass_ é inválida.</span><span class="sxs-lookup"><span data-stu-id="84ab9-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="84ab9-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="84ab9-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="84ab9-124">O objeto status não oferece suporte a essa operação, conforme indicado pela ausência do sinalizador STATUS_CHANGE_PASSWORD na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.</span><span class="sxs-lookup"><span data-stu-id="84ab9-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84ab9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="84ab9-125">Remarks</span></span>

<span data-ttu-id="84ab9-126">Nem todos os objetos de status dão suporte ao método **IMAPIStatus:: ChangePassword** .</span><span class="sxs-lookup"><span data-stu-id="84ab9-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="84ab9-127">Só há suporte para os provedores de serviços que exigem que os clientes insiram uma senha.</span><span class="sxs-lookup"><span data-stu-id="84ab9-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="84ab9-128">Nenhum dos objetos de status que o MAPI implementa oferece suporte à operação de alteração de senha.</span><span class="sxs-lookup"><span data-stu-id="84ab9-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="84ab9-129">**ChangePassword** modifica uma senha por meio de programação, sem interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="84ab9-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84ab9-130">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="84ab9-130">Notes to implementers</span></span>

<span data-ttu-id="84ab9-131">Os provedores de transporte remotos implementam a **ChangePassword** conforme especificado aqui.</span><span class="sxs-lookup"><span data-stu-id="84ab9-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="84ab9-132">Não há considerações especiais.</span><span class="sxs-lookup"><span data-stu-id="84ab9-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84ab9-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="84ab9-133">See also</span></span>



[<span data-ttu-id="84ab9-134">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="84ab9-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="84ab9-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="84ab9-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

