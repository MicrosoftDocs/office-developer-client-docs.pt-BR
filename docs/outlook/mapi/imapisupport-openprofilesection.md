---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767264"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="f82fe-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="f82fe-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="f82fe-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f82fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f82fe-105">Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="f82fe-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="f82fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f82fe-106">Parameters</span></span>

 <span data-ttu-id="f82fe-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="f82fe-107">_lpUid_</span></span>
  
> <span data-ttu-id="f82fe-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil para ser aberto.</span><span class="sxs-lookup"><span data-stu-id="f82fe-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="f82fe-109">Passar NULL para o parâmetro _lpUid_ abre a seção de perfil do chamador.</span><span class="sxs-lookup"><span data-stu-id="f82fe-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="f82fe-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f82fe-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f82fe-111">[in] Uma bitmask dos sinalizadores que controla como a seção de perfil é aberta.</span><span class="sxs-lookup"><span data-stu-id="f82fe-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="f82fe-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f82fe-112">The following flags can be set:</span></span>
    
<span data-ttu-id="f82fe-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f82fe-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f82fe-114">Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente acessível ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f82fe-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="f82fe-115">Se a seção de perfil não está acessível, fazendo uma chamada do objeto subsequente pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="f82fe-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="f82fe-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f82fe-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f82fe-117">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="f82fe-117">Requests read/write permission.</span></span> <span data-ttu-id="f82fe-118">Por padrão, os objetos são abertos como somente leitura e os chamadores não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f82fe-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="f82fe-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="f82fe-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="f82fe-120">[out] Um ponteiro para um ponteiro para a seção perfil aberta.</span><span class="sxs-lookup"><span data-stu-id="f82fe-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f82fe-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f82fe-121">Return value</span></span>

<span data-ttu-id="f82fe-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f82fe-122">S_OK</span></span> 
  
> <span data-ttu-id="f82fe-123">Seção perfil tiver sido aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="f82fe-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="f82fe-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f82fe-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f82fe-125">Foi feita uma tentativa para modificar uma seção de perfil de somente leitura ou para acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="f82fe-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="f82fe-126">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f82fe-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f82fe-127">Não há uma seção de perfil associada com o identificador de entrada passado _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="f82fe-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="f82fe-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f82fe-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="f82fe-129">Reservado ou não há suporte para sinalizadores foram usadas e, portanto, a operação não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f82fe-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f82fe-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="f82fe-130">Remarks</span></span>

<span data-ttu-id="f82fe-131">O método **IMAPISupport::OpenProfileSection** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="f82fe-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="f82fe-132">Provedores de serviço e serviços de mensagem chamada **OpenProfileSection** para abrir uma seção de perfil e recuperar um ponteiro para sua implementação de interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="f82fe-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f82fe-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f82fe-133">Notes to callers</span></span>

 <span data-ttu-id="f82fe-134">**OpenProfileSection** abre seções de perfil como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY no parâmetro _ulFlags_ e sua permissão é suficiente.</span><span class="sxs-lookup"><span data-stu-id="f82fe-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="f82fe-135">Defina esse sinalizador não garante a permissão de leitura/gravação; as permissões são concedidas dependem do seu nível de acesso e o objeto.</span><span class="sxs-lookup"><span data-stu-id="f82fe-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="f82fe-136">Se **OpenProfileSection** tenta abrir uma seção de perfil inexistente como somente leitura, ele retornará E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="f82fe-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="f82fe-137">Se **OpenProfileSection** tenta abrir uma seção de perfil inexistente como leitura/gravação, ele cria a seção de perfil e retorna o ponteiro **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="f82fe-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f82fe-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f82fe-138">See also</span></span>



[<span data-ttu-id="f82fe-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f82fe-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="f82fe-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f82fe-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="f82fe-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f82fe-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f82fe-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f82fe-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

