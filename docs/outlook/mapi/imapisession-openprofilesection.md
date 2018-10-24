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
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568186"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="a6034-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a6034-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="a6034-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6034-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6034-105">Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="a6034-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="a6034-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6034-106">Parameters</span></span>

 <span data-ttu-id="a6034-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a6034-107">_lpUID_</span></span>
  
> <span data-ttu-id="a6034-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="a6034-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="a6034-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a6034-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a6034-110">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="a6034-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="a6034-111">Passar NULL faz com que o parâmetro _lppProfSect_ retornar um ponteiro para a interface da seção perfil padrão, **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="a6034-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="a6034-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6034-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a6034-113">[in] Uma bitmask dos sinalizadores que controla o acesso à seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="a6034-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="a6034-114">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a6034-114">The following flags can be set:</span></span>
    
<span data-ttu-id="a6034-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a6034-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a6034-116">Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="a6034-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="a6034-117">Se o perfil da seção não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="a6034-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="a6034-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a6034-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="a6034-119">Permite o acesso a uma seção de perfil que não pertencem ao provedor.</span><span class="sxs-lookup"><span data-stu-id="a6034-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="a6034-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a6034-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a6034-121">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="a6034-121">Requests read/write permission.</span></span> <span data-ttu-id="a6034-122">Por padrão, seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a6034-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a6034-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="a6034-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="a6034-124">[out] Um ponteiro para um ponteiro para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="a6034-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6034-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a6034-125">Return value</span></span>

<span data-ttu-id="a6034-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6034-126">S_OK</span></span> 
  
> <span data-ttu-id="a6034-127">Seção perfil tiver sido aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="a6034-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="a6034-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a6034-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a6034-129">Foi feita uma tentativa de acessar uma seção de perfil para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="a6034-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="a6034-130">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a6034-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a6034-131">A seção de perfil solicitada não existe.</span><span class="sxs-lookup"><span data-stu-id="a6034-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6034-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6034-132">Remarks</span></span>

<span data-ttu-id="a6034-133">O método **IMAPISession::OpenProfileSection** abre uma seção de perfil ou o objeto que dá suporte à interface **IProfSect** .</span><span class="sxs-lookup"><span data-stu-id="a6034-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="a6034-134">As seções de perfil são usadas para ler informações do e gravando informações do perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6034-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="a6034-135">Você não pode usar **OpenProfileSection** para abrir seções de perfil que próprio de provedores de serviços individuais, a menos que você especifique MAPI_FORCE_ACCESS no parâmetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a6034-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6034-136">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a6034-136">Notes to callers</span></span>

<span data-ttu-id="a6034-137">Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a6034-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="a6034-138">Se outro cliente tiver uma seção de perfil abra se você tenta abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada irá falhar, retornando MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="a6034-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="a6034-139">Uma operação de abertura somente leitura falhará se a seção está aberta para gravação.</span><span class="sxs-lookup"><span data-stu-id="a6034-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="a6034-140">Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura **MAPIUID** inexistente no parâmetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="a6034-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="a6034-141">Certifique-se de que você especifique MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="a6034-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="a6034-142">Se você definir _lpUID_ para apontar para um inexistente **MAPIUID** e **OpenProfileSection** está definido para usar o modo de padrão de acesso de somente leitura, a chamada irá falhar com MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="a6034-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6034-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6034-143">See also</span></span>



[<span data-ttu-id="a6034-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6034-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="a6034-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6034-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="a6034-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a6034-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a6034-147">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6034-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

