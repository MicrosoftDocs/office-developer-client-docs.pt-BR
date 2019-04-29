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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411383"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="9b863-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9b863-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="9b863-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b863-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b863-105">Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="9b863-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="9b863-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b863-106">Parameters</span></span>

 <span data-ttu-id="9b863-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="9b863-107">_lpUid_</span></span>
  
> <span data-ttu-id="9b863-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="9b863-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="9b863-109">Passar NULL para o parâmetro _lpUid_ abre a seção de perfil do chamador.</span><span class="sxs-lookup"><span data-stu-id="9b863-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="9b863-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b863-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9b863-111">no Uma bitmask de sinalizadores que controla como a seção de perfil é aberta.</span><span class="sxs-lookup"><span data-stu-id="9b863-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="9b863-112">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9b863-112">The following flags can be set:</span></span>
    
<span data-ttu-id="9b863-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9b863-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9b863-114">Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes da seção de perfil ser totalmente acessível ao chamador.</span><span class="sxs-lookup"><span data-stu-id="9b863-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="9b863-115">Se a seção Profile não estiver acessível, fazer uma chamada de objeto subsequente pode resultar em um erro.</span><span class="sxs-lookup"><span data-stu-id="9b863-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="9b863-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9b863-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9b863-117">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9b863-117">Requests read/write permission.</span></span> <span data-ttu-id="9b863-118">Por padrão, os objetos são abertos como somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="9b863-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="9b863-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="9b863-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="9b863-120">bota Um ponteiro para um ponteiro para a seção de perfil aberta.</span><span class="sxs-lookup"><span data-stu-id="9b863-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b863-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9b863-121">Return value</span></span>

<span data-ttu-id="9b863-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b863-122">S_OK</span></span> 
  
> <span data-ttu-id="9b863-123">A seção de perfil foi aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="9b863-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="9b863-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9b863-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9b863-125">Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou para acessar um objeto para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="9b863-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="9b863-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9b863-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9b863-127">Não há uma seção de perfil associada ao identificador de entrada passado no _lpEntryID_.</span><span class="sxs-lookup"><span data-stu-id="9b863-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="9b863-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="9b863-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="9b863-129">Sinalizadores reservados ou não suportados foram usados e, portanto, a operação não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9b863-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b863-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b863-130">Remarks</span></span>

<span data-ttu-id="9b863-131">O método **IMAPISupport:: OpenProfileSection** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="9b863-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="9b863-132">Os provedores de serviços e serviços de mensagens chamam o **OpenProfileSection** para abrir uma seção de perfil e recuperar um ponteiro para sua implementação de interface do **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="9b863-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b863-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9b863-133">Notes to callers</span></span>

 <span data-ttu-id="9b863-134">O **OpenProfileSection** abre seções de perfil como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY no parâmetro _parâmetroulflags_ e sua permissão seja suficiente.</span><span class="sxs-lookup"><span data-stu-id="9b863-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="9b863-135">A configuração desse sinalizador não garante permissão de leitura/gravação; as permissões que você recebe dependem do seu nível de acesso e do objeto.</span><span class="sxs-lookup"><span data-stu-id="9b863-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="9b863-136">Se o **OpenProfileSection** tentar abrir uma seção de perfil não existente como somente leitura, ele retornará MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="9b863-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="9b863-137">Se o **OpenProfileSection** tentar abrir uma seção de perfil não existente como leitura/gravação, ele criará a seção Profile e retornará o ponteiro **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="9b863-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b863-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b863-138">See also</span></span>



[<span data-ttu-id="9b863-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b863-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="9b863-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b863-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="9b863-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9b863-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9b863-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b863-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

