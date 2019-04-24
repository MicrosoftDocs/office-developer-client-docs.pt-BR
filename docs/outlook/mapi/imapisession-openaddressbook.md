---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329418"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="6d824-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="6d824-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="6d824-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d824-105">Abre o catálogo de endereços integrado MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="6d824-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="6d824-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d824-106">Parameters</span></span>

 <span data-ttu-id="6d824-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6d824-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6d824-108">no Uma alça para a janela pai da caixa de diálogo endereço comum e outros vídeos relacionados.</span><span class="sxs-lookup"><span data-stu-id="6d824-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="6d824-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6d824-109">_lpInterface_</span></span>
  
> <span data-ttu-id="6d824-110">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d824-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="6d824-111">Passar **nulo** retorna um ponteiro para a interface padrão do catálogo de endereços, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6d824-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="6d824-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6d824-112">_ulFlags_</span></span>
  
> <span data-ttu-id="6d824-113">no Uma bitmask de sinalizadores que controla a abertura do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d824-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="6d824-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6d824-114">The following flag can be set:</span></span>
    
<span data-ttu-id="6d824-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6d824-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="6d824-116">SuPrime a exibição de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d824-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="6d824-117">Se o sinalizador AB_NO_DIALOG não estiver definido, os provedores de catálogo de endereços que contribuem para o catálogo de endereços integrado podem solicitar que o usuário Verifique as informações necessárias.</span><span class="sxs-lookup"><span data-stu-id="6d824-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="6d824-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="6d824-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="6d824-119">bota Um ponteiro para um ponteiro para o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d824-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d824-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6d824-120">Return value</span></span>

<span data-ttu-id="6d824-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d824-121">S_OK</span></span> 
  
> <span data-ttu-id="6d824-122">O catálogo de endereços foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="6d824-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="6d824-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6d824-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6d824-124">A chamada foi bem-sucedida, mas não foi possível abrir os contêineres de um ou mais provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d824-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="6d824-125">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6d824-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="6d824-126">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="6d824-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="6d824-127">Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="6d824-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d824-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d824-128">Remarks</span></span>

<span data-ttu-id="6d824-129">O método **IMAPISession:: OpenAddressBook** abre o catálogo de endereços integrado MAPI, uma coleção dos contêineres de nível superior de todos os provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="6d824-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="6d824-130">O ponteiro retornado no parâmetro _lppAdrBook_ fornece acesso adicional ao conteúdo do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="6d824-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="6d824-131">Isso permite que o chamador realize tarefas como abrir contêineres individuais, localizar usuários de mensagens e exibir caixas de diálogo de endereços comuns.</span><span class="sxs-lookup"><span data-stu-id="6d824-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6d824-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6d824-132">Notes to callers</span></span>

 <span data-ttu-id="6d824-133">**OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED se não puder carregar um ou mais dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="6d824-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="6d824-134">Esse valor é um aviso, não um valor de erro; manipule-o como seria de S_OK.</span><span class="sxs-lookup"><span data-stu-id="6d824-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="6d824-135">**OpenAddressBook** sempre retorna um ponteiro válido no parâmetro _lppAdrBook_ , independentemente de quantos dos provedores de catálogo de endereços não puderam ser carregados.</span><span class="sxs-lookup"><span data-stu-id="6d824-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="6d824-136">Portanto, você deve sempre chamar o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do catálogo de endereços em algum momento antes de fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="6d824-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="6d824-137">Quando **OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED, chame [IMAPISession:: GetLastError](imapisession-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores com falha.</span><span class="sxs-lookup"><span data-stu-id="6d824-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="6d824-138">Uma única estrutura **MAPIERROR** é retornada, contendo informações fornecidas por todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="6d824-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6d824-139">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6d824-139">MFCMAPI reference</span></span>

<span data-ttu-id="6d824-140">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d824-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6d824-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="6d824-141">**File**</span></span>|<span data-ttu-id="6d824-142">**Função**</span><span class="sxs-lookup"><span data-stu-id="6d824-142">**Function**</span></span>|<span data-ttu-id="6d824-143">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="6d824-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d824-144">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="6d824-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6d824-145">CMapiObjects:: GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="6d824-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="6d824-146">MFCMAPI usa o método **IMAPISession:: OpenAddressBook** para obter o catálogo de endereços integrado.</span><span class="sxs-lookup"><span data-stu-id="6d824-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d824-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d824-147">See also</span></span>



[<span data-ttu-id="6d824-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6d824-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="6d824-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6d824-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="6d824-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6d824-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6d824-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6d824-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6d824-152">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="6d824-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

