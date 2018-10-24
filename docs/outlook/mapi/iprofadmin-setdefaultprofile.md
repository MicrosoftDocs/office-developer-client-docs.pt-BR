---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587702"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="6f395-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f395-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="6f395-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f395-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f395-105">Define ou limpa o perfil padrão de um cliente.</span><span class="sxs-lookup"><span data-stu-id="6f395-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6f395-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f395-106">Parameters</span></span>

 <span data-ttu-id="6f395-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="6f395-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="6f395-108">[in] Um ponteiro para o nome do perfil que será se tornam o padrão ou NULL.</span><span class="sxs-lookup"><span data-stu-id="6f395-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="6f395-109">A definição de _lpszProfileName_ como nulo indica que o **SetDefaultProfile** deve remover o perfil padrão existente, deixando o cliente sem um padrão.</span><span class="sxs-lookup"><span data-stu-id="6f395-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="6f395-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f395-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6f395-111">[in] Uma bitmask dos sinalizadores que controla o tipo da cadeia de caracteres apontado pela _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="6f395-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="6f395-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6f395-112">The following flag can be set:</span></span>
    
<span data-ttu-id="6f395-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6f395-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6f395-114">O nome do perfil está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6f395-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="6f395-115">Se o sinalizador MAPI_UNICODE não estiver definido, o nome de perfil é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6f395-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6f395-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6f395-116">Return value</span></span>

<span data-ttu-id="6f395-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f395-117">S_OK</span></span> 
  
> <span data-ttu-id="6f395-118">Um perfil padrão foi estabelecido ou removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="6f395-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="6f395-119">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6f395-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6f395-120">O perfil especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="6f395-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f395-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f395-121">Remarks</span></span>

<span data-ttu-id="6f395-122">O método **IProfAdmin::SetDefaultProfile** estabelece um perfil específico como o perfil do cliente padrão ou limpa o perfil padrão atual.</span><span class="sxs-lookup"><span data-stu-id="6f395-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="6f395-123">O perfil padrão é o perfil que será usado automaticamente sempre que o cliente inicia uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="6f395-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="6f395-124">**SetDefaultProfile** também define a propriedade de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) do novo perfil padrão como TRUE.</span><span class="sxs-lookup"><span data-stu-id="6f395-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6f395-125">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6f395-125">Notes to callers</span></span>

<span data-ttu-id="6f395-126">Para iniciar uma sessão com o perfil padrão, passe o sinalizador MAPI_USE_DEFAULT para a função [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="6f395-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6f395-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f395-127">See also</span></span>



[<span data-ttu-id="6f395-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="6f395-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="6f395-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6f395-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="6f395-130">Propriedade canônico de PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f395-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="6f395-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f395-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

