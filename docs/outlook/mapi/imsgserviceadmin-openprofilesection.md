---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437109"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="1a4f0-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1a4f0-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="1a4f0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a4f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a4f0-105">Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="1a4f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a4f0-106">Parameters</span></span>

 <span data-ttu-id="1a4f0-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="1a4f0-107">_lpUID_</span></span>
  
> <span data-ttu-id="1a4f0-108">Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="1a4f0-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1a4f0-109">_lpInterface_</span></span>
  
> <span data-ttu-id="1a4f0-110">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="1a4f0-111">Passar resultados nulos em um ponteiro para a interface padrão que está sendo retornada no parâmetro _lppProfSect_ .</span><span class="sxs-lookup"><span data-stu-id="1a4f0-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="1a4f0-112">A interface padrão para uma seção de perfil é **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="1a4f0-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a4f0-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1a4f0-114">no Uma bitmask de sinalizadores que controla o acesso à seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="1a4f0-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1a4f0-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1a4f0-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1a4f0-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1a4f0-117">Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes que a seção de perfil esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="1a4f0-118">Se a seção de perfil não estiver disponível, fazer uma chamada subsequente para ela poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="1a4f0-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1a4f0-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="1a4f0-120">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-120">Requests read/write permission.</span></span> <span data-ttu-id="1a4f0-121">Por padrão, as seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="1a4f0-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1a4f0-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="1a4f0-123">Permite o acesso a todas as seções de perfil, mesmo aquelas pertencentes a provedores de serviços individuais.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="1a4f0-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="1a4f0-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="1a4f0-125">bota Um ponteiro para um ponteiro para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a4f0-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1a4f0-126">Return value</span></span>

<span data-ttu-id="1a4f0-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a4f0-127">S_OK</span></span> 
  
> <span data-ttu-id="1a4f0-128">A seção de perfil foi aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="1a4f0-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1a4f0-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1a4f0-130">Foi feita uma tentativa de acessar uma seção de perfil para a qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="1a4f0-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1a4f0-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1a4f0-132">A seção de perfil solicitada não existe.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a4f0-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a4f0-133">Remarks</span></span>

<span data-ttu-id="1a4f0-134">O método **IMsgServiceAdmin:: OpenProfileSection** abre uma seção de perfil, um objeto que dá suporte à interface [IProfSect](iprofsectimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4f0-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="1a4f0-135">Seções de perfil são usadas para ler informações de e gravar informações no perfil de sessão.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="1a4f0-136">**OpenProfileSection** não pode ser usado para abrir seções de perfil pertencentes a provedores de serviço individuais, a menos que o MAPI_FORCE_ACCESS seja usado.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a4f0-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1a4f0-137">Notes to callers</span></span>

<span data-ttu-id="1a4f0-138">Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="1a4f0-139">Se outro cliente tiver uma seção de perfil aberta que você tentar abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada falhará, retornando MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="1a4f0-140">Uma operação de abertura somente leitura falhará se a seção estiver aberta para gravação.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="1a4f0-141">Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura [MAPIUID](mapiuid.md) inexistente no parâmetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="1a4f0-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="1a4f0-142">Certifique-se de especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="1a4f0-143">Se você definir _lpUID_ para apontar para um **MAPIUID** não existente e o **OpenProfileSection** estiver definido para usar o modo de acesso padrão de somente leitura, a chamada falhará com o MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1a4f0-144">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1a4f0-144">MFCMAPI reference</span></span>

<span data-ttu-id="1a4f0-145">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1a4f0-146">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1a4f0-146">**File**</span></span>|<span data-ttu-id="1a4f0-147">**Função**</span><span class="sxs-lookup"><span data-stu-id="1a4f0-147">**Function**</span></span>|<span data-ttu-id="1a4f0-148">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1a4f0-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1a4f0-149">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="1a4f0-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1a4f0-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1a4f0-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="1a4f0-151">MFCMAPI usa o método **IMsgServiceAdmin:: OpenProfileSection** para abrir uma seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="1a4f0-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a4f0-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a4f0-152">See also</span></span>



[<span data-ttu-id="1a4f0-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a4f0-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="1a4f0-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1a4f0-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="1a4f0-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1a4f0-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="1a4f0-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1a4f0-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1a4f0-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a4f0-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="1a4f0-158">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1a4f0-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

