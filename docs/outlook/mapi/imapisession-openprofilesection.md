---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439916"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="108ca-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="108ca-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="108ca-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="108ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="108ca-105">Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="108ca-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="108ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="108ca-106">Parameters</span></span>

 <span data-ttu-id="108ca-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="108ca-107">_lpUID_</span></span>
  
> <span data-ttu-id="108ca-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="108ca-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="108ca-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="108ca-109">_lpInterface_</span></span>
  
> <span data-ttu-id="108ca-110">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="108ca-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="108ca-111">Passar NULL faz com que o parâmetro _lppProfSect_ retorne um ponteiro para a interface padrão da seção de perfil, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="108ca-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="108ca-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="108ca-112">_ulFlags_</span></span>
  
> <span data-ttu-id="108ca-113">no Uma bitmask de sinalizadores que controla o acesso à seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="108ca-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="108ca-114">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="108ca-114">The following flags can be set:</span></span>
    
<span data-ttu-id="108ca-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="108ca-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="108ca-116">Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes que a seção de perfil esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="108ca-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="108ca-117">Se a seção de perfil não estiver disponível, fazer uma chamada subsequente para ela poderá causar um erro.</span><span class="sxs-lookup"><span data-stu-id="108ca-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="108ca-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="108ca-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="108ca-119">Permite o acesso a uma seção de perfil que não pertence ao provedor.</span><span class="sxs-lookup"><span data-stu-id="108ca-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="108ca-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="108ca-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="108ca-121">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="108ca-121">Requests read/write permission.</span></span> <span data-ttu-id="108ca-122">Por padrão, as seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="108ca-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="108ca-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="108ca-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="108ca-124">bota Um ponteiro para um ponteiro para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="108ca-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="108ca-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="108ca-125">Return value</span></span>

<span data-ttu-id="108ca-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="108ca-126">S_OK</span></span> 
  
> <span data-ttu-id="108ca-127">A seção de perfil foi aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="108ca-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="108ca-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="108ca-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="108ca-129">Foi feita uma tentativa de acessar uma seção de perfil para a qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="108ca-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="108ca-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="108ca-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="108ca-131">A seção de perfil solicitada não existe.</span><span class="sxs-lookup"><span data-stu-id="108ca-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="108ca-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="108ca-132">Remarks</span></span>

<span data-ttu-id="108ca-133">O método **IMAPISession:: OpenProfileSection** abre uma seção ou um objeto de perfil que oferece suporte à interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="108ca-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="108ca-134">Seções de perfil são usadas para ler informações de e gravar informações no perfil de sessão.</span><span class="sxs-lookup"><span data-stu-id="108ca-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="108ca-135">Você não pode usar **OpenProfileSection** para abrir seções de perfil que provedores de serviços individuais, a menos que você especifique MAPI_FORCE_ACCESS no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="108ca-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="108ca-136">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="108ca-136">Notes to callers</span></span>

<span data-ttu-id="108ca-137">Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="108ca-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="108ca-138">Se outro cliente tiver uma seção de perfil aberta que você tentar abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada falhará, retornando MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="108ca-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="108ca-139">Uma operação de abertura somente leitura falhará se a seção estiver aberta para gravação.</span><span class="sxs-lookup"><span data-stu-id="108ca-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="108ca-140">Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura **MAPIUID** inexistente no parâmetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="108ca-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="108ca-141">Certifique-se de especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="108ca-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="108ca-142">Se você definir _lpUID_ para apontar para um **MAPIUID** não existente e o **OpenProfileSection** estiver definido para usar o modo de acesso padrão de somente leitura, a chamada falhará com o MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="108ca-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="108ca-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="108ca-143">See also</span></span>



[<span data-ttu-id="108ca-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="108ca-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="108ca-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="108ca-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="108ca-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="108ca-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="108ca-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="108ca-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

