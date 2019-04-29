---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405657"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="7727c-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7727c-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="7727c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7727c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7727c-105">Abre uma seção de perfil do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="7727c-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="7727c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7727c-106">Parameters</span></span>

 <span data-ttu-id="7727c-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="7727c-107">_lpUID_</span></span>
  
> <span data-ttu-id="7727c-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo da seção de perfil a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="7727c-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="7727c-109">Os clientes não devem passar NULL para o parâmetro _lpUID_ .</span><span class="sxs-lookup"><span data-stu-id="7727c-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="7727c-110">Os provedores de serviços podem passar NULL para recuperar o **MAPIUID** quando chamam de suas funções de ponto de entrada de serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7727c-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="7727c-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7727c-111">_lpInterface_</span></span>
  
> <span data-ttu-id="7727c-112">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="7727c-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="7727c-113">Passar resultados nulos na interface padrão da seção de perfil (**IProfSect**) que está sendo retornada.</span><span class="sxs-lookup"><span data-stu-id="7727c-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="7727c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7727c-114">_ulFlags_</span></span>
  
> <span data-ttu-id="7727c-115">no Uma bitmask de sinalizadores que controla como a seção de perfil é aberta.</span><span class="sxs-lookup"><span data-stu-id="7727c-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="7727c-116">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7727c-116">The following flags can be set:</span></span>
    
<span data-ttu-id="7727c-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7727c-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7727c-118">Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes que a seção de perfil esteja totalmente disponível para o chamador.</span><span class="sxs-lookup"><span data-stu-id="7727c-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="7727c-119">Se a seção de perfil não estiver disponível, fazer uma chamada subsequente para ela poderá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="7727c-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="7727c-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="7727c-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="7727c-121">Solicita permissão de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7727c-121">Requests read/write permission.</span></span> <span data-ttu-id="7727c-122">Por padrão, os objetos são abertos com permissão somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida.</span><span class="sxs-lookup"><span data-stu-id="7727c-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="7727c-123">Os clientes não têm permissão de leitura/gravação para seções de provedor do perfil.</span><span class="sxs-lookup"><span data-stu-id="7727c-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="7727c-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7727c-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="7727c-125">Permite o acesso a todas as seções de perfil, mesmo aquelas pertencentes a provedores de serviços individuais.</span><span class="sxs-lookup"><span data-stu-id="7727c-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="7727c-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="7727c-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="7727c-127">bota Um ponteiro para um ponteiro para a seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="7727c-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7727c-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7727c-128">Return value</span></span>

<span data-ttu-id="7727c-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="7727c-129">S_OK</span></span> 
  
> <span data-ttu-id="7727c-130">A seção de perfil foi aberta com êxito.</span><span class="sxs-lookup"><span data-stu-id="7727c-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="7727c-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7727c-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7727c-132">Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.</span><span class="sxs-lookup"><span data-stu-id="7727c-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="7727c-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7727c-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7727c-134">A seção de perfil solicitada não existe.</span><span class="sxs-lookup"><span data-stu-id="7727c-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7727c-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="7727c-135">Remarks</span></span>

<span data-ttu-id="7727c-136">O método **IProviderAdmin:: OpenProfileSection** abre uma seção de perfil, permitindo que o chamador Leia informações e, possivelmente, grave informações no perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="7727c-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="7727c-137">Os clientes não podem abrir seções de perfil que pertencem a provedores usando o método **OpenProfileSection** .</span><span class="sxs-lookup"><span data-stu-id="7727c-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="7727c-138">Vários clientes ou provedores de serviço podem abrir simultaneamente uma seção de perfil com permissão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7727c-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="7727c-139">No enTanto, quando uma seção de perfil é aberta com permissão de leitura/gravação, nenhuma outra chamada pode ser feita para abrir a seção, independentemente do tipo de acesso.</span><span class="sxs-lookup"><span data-stu-id="7727c-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="7727c-140">Se uma seção de perfil estiver aberta com permissão somente leitura, uma chamada subsequente para solicitar permissão de leitura/gravação falhará com o MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="7727c-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="7727c-141">Da mesma forma, se uma seção estiver aberta com permissão de leitura/gravação, uma chamada subsequente para solicitar permissão somente leitura também falhará.</span><span class="sxs-lookup"><span data-stu-id="7727c-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7727c-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7727c-142">Notes to callers</span></span>

<span data-ttu-id="7727c-143">Se você solicitar que **OpenProfileSection** abra uma seção de perfil não existente passando MAPI_MODIFY no _Parâmetroulflags_ e um **MAPIUID** desconhecido no _lpUID_, a seção de perfil será criada.</span><span class="sxs-lookup"><span data-stu-id="7727c-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="7727c-144">Se você solicitar que **OpenProfileSection** abra uma seção não existente com permissão somente leitura, ele retornará MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="7727c-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7727c-145">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7727c-145">MFCMAPI reference</span></span>

<span data-ttu-id="7727c-146">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7727c-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7727c-147">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7727c-147">**File**</span></span>|<span data-ttu-id="7727c-148">**Função**</span><span class="sxs-lookup"><span data-stu-id="7727c-148">**Function**</span></span>|<span data-ttu-id="7727c-149">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7727c-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7727c-150">MAPIProfileFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="7727c-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7727c-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7727c-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="7727c-152">MFCMAPI usa o método **IProviderAdmin:: OpenProfileSection** para abrir uma seção de perfil do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="7727c-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7727c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="7727c-153">See also</span></span>



[<span data-ttu-id="7727c-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7727c-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="7727c-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7727c-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="7727c-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7727c-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="7727c-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7727c-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="7727c-158">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7727c-158">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

