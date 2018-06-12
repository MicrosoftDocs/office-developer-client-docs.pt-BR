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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767470"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="8e699-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8e699-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="8e699-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e699-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e699-105">Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="8e699-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="8e699-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8e699-106">Parameters</span></span>

 <span data-ttu-id="8e699-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="8e699-107">_lpUID_</span></span>
  
> <span data-ttu-id="8e699-108">Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="8e699-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="8e699-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8e699-109">_lpInterface_</span></span>
  
> <span data-ttu-id="8e699-110">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="8e699-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="8e699-111">Passagem nula resulta em um ponteiro para sua interface padrão que está sendo retornada no parâmetro _lppProfSect_ .</span><span class="sxs-lookup"><span data-stu-id="8e699-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="8e699-112">A interface padrão para uma seção de perfil é **IProfSect**.</span><span class="sxs-lookup"><span data-stu-id="8e699-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="8e699-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e699-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8e699-114">[in] Uma bitmask dos sinalizadores que controla o acesso à seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="8e699-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="8e699-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="8e699-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8e699-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8e699-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8e699-117">Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="8e699-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="8e699-118">Se o perfil da seção não estiver disponível, fazendo uma chamada subsequente a ele pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="8e699-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="8e699-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8e699-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8e699-120">Permissão de leitura/gravação solicitações.</span><span class="sxs-lookup"><span data-stu-id="8e699-120">Requests read/write permission.</span></span> <span data-ttu-id="8e699-121">Por padrão, seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e699-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="8e699-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8e699-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="8e699-123">Permite o acesso a todas as seções de perfil, mesmo aqueles pertencentes a provedores de serviços individuais.</span><span class="sxs-lookup"><span data-stu-id="8e699-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="8e699-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="8e699-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="8e699-125">[out] Um ponteiro para um ponteiro para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="8e699-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e699-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8e699-126">Return value</span></span>

<span data-ttu-id="8e699-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e699-127">S_OK</span></span> 
  
> <span data-ttu-id="8e699-128">Seção perfil tiver sido aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="8e699-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="8e699-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8e699-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8e699-130">Foi feita uma tentativa de acessar uma seção de perfil para o qual o chamador tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="8e699-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="8e699-131">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8e699-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8e699-132">A seção de perfil solicitada não existe.</span><span class="sxs-lookup"><span data-stu-id="8e699-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e699-133">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="8e699-133">Remarks</span></span>

<span data-ttu-id="8e699-134">O método **IMsgServiceAdmin::OpenProfileSection** abre uma seção de perfil, um objeto que dá suporte à interface [IProfSect](iprofsectimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="8e699-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="8e699-135">As seções de perfil são usadas para ler informações do e gravando informações do perfil da sessão.</span><span class="sxs-lookup"><span data-stu-id="8e699-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="8e699-136">**OpenProfileSection** não pode ser usado para abrir seções perfil pertencentes a provedores de serviços individuais, a menos que MAPI_FORCE_ACCESS é usado.</span><span class="sxs-lookup"><span data-stu-id="8e699-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e699-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8e699-137">Notes to callers</span></span>

<span data-ttu-id="8e699-138">Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e699-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="8e699-139">Se outro cliente tiver uma seção de perfil abra se você tenta abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada irá falhar, retornando MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="8e699-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="8e699-140">Uma operação de abertura somente leitura falhará se a seção está aberta para gravação.</span><span class="sxs-lookup"><span data-stu-id="8e699-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="8e699-141">Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura [MAPIUID](mapiuid.md) inexistente no parâmetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="8e699-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="8e699-142">Certifique-se de que você especificar MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="8e699-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="8e699-143">Se você definir _lpUID_ para apontar para um inexistente **MAPIUID** e **OpenProfileSection** está definido para usar o modo de padrão de acesso de somente leitura, a chamada irá falhar com MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="8e699-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8e699-144">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8e699-144">MFCMAPI reference</span></span>

<span data-ttu-id="8e699-145">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e699-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8e699-146">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="8e699-146">**File**</span></span>|<span data-ttu-id="8e699-147">**Function**</span><span class="sxs-lookup"><span data-stu-id="8e699-147">**Function**</span></span>|<span data-ttu-id="8e699-148">**Comment**</span><span class="sxs-lookup"><span data-stu-id="8e699-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8e699-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8e699-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8e699-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8e699-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="8e699-151">MFCMAPI usa o método **IMsgServiceAdmin::OpenProfileSection** para abrir uma seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="8e699-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e699-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e699-152">See also</span></span>



[<span data-ttu-id="8e699-153">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e699-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8e699-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8e699-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="8e699-155">IProfSect: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8e699-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="8e699-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8e699-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8e699-157">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e699-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="8e699-158">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="8e699-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

