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
ms.openlocfilehash: dcde242f5f2e956d1926d6914431008383f5aa55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767178"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="1f601-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="1f601-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="1f601-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f601-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f601-105">Abre o catálogo de endereços integrada de MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="1f601-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="1f601-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f601-106">Parameters</span></span>

 <span data-ttu-id="1f601-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1f601-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1f601-108">[in] Um identificador para a janela do pai da caixa de diálogo endereço comuns e outros relacionados a exibe.</span><span class="sxs-lookup"><span data-stu-id="1f601-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="1f601-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1f601-109">_lpInterface_</span></span>
  
> <span data-ttu-id="1f601-110">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1f601-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="1f601-111">Passar **Nulo** retorna um ponteiro para a interface de padrão do catálogo de endereços, [IAddrBook: IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="1f601-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="1f601-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f601-112">_ulFlags_</span></span>
  
> <span data-ttu-id="1f601-113">[in] Uma bitmask dos sinalizadores que controla a abertura do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1f601-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="1f601-114">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="1f601-114">The following flag can be set:</span></span>
    
<span data-ttu-id="1f601-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1f601-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="1f601-116">Suprime a exibição das caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1f601-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="1f601-117">Se o sinalizador AB_NO_DIALOG não estiver definido, os provedores de catálogo de endereços que contribuem para o catálogo de endereços integrada podem solicitar ao usuário de qualquer informação necessária.</span><span class="sxs-lookup"><span data-stu-id="1f601-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="1f601-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="1f601-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="1f601-119">[out] Um ponteiro para um ponteiro para o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1f601-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1f601-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1f601-120">Return value</span></span>

<span data-ttu-id="1f601-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f601-121">S_OK</span></span> 
  
> <span data-ttu-id="1f601-122">O catálogo de endereços foi aberto com êxito.</span><span class="sxs-lookup"><span data-stu-id="1f601-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="1f601-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1f601-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1f601-124">A chamada foi bem-sucedida, mas os contêineres de um ou mais provedores de catálogo de endereços não pôde ser abertos.</span><span class="sxs-lookup"><span data-stu-id="1f601-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="1f601-125">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1f601-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1f601-126">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="1f601-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1f601-127">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1f601-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f601-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f601-128">Remarks</span></span>

<span data-ttu-id="1f601-129">O método **IMAPISession::OpenAddressBook** abre o catálogo de endereços integrada de MAPI, uma coleção dos contêineres de todos os provedores de catálogo de endereços no perfil de nível superior.</span><span class="sxs-lookup"><span data-stu-id="1f601-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="1f601-130">O ponteiro retornado no parâmetro _lppAdrBook_ fornece mais acesso ao conteúdo do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1f601-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="1f601-131">Isso permite que o chamador realizar tarefas como contêineres individuais de abertura, os usuários de mensagens de localização e exibindo caixas de diálogo comuns do endereço.</span><span class="sxs-lookup"><span data-stu-id="1f601-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1f601-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1f601-132">Notes to callers</span></span>

 <span data-ttu-id="1f601-133">**OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED se ele não é possível carregar um ou mais dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="1f601-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="1f601-134">Esse valor é um aviso, não é um valor de erro; lidar com ele como faria S_OK.</span><span class="sxs-lookup"><span data-stu-id="1f601-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="1f601-135">**OpenAddressBook** sempre retorna um ponteiro válido no parâmetro _lppAdrBook_ , independentemente de quantos dos provedores de catálogo de endereços a falha ao carregar.</span><span class="sxs-lookup"><span data-stu-id="1f601-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="1f601-136">Portanto, você sempre deve chamar método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) do catálogo de endereços em algum momento antes de fazer logoff.</span><span class="sxs-lookup"><span data-stu-id="1f601-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="1f601-137">Quando **OpenAddressBook** retorna MAPI_W_ERRORS_RETURNED, chame [IMAPISession::GetLastError](imapisession-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores de falha.</span><span class="sxs-lookup"><span data-stu-id="1f601-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="1f601-138">Uma estrutura **MAPIERROR** única é retornada que contém as informações fornecidas pelo todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="1f601-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f601-139">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1f601-139">MFCMAPI reference</span></span>

<span data-ttu-id="1f601-140">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f601-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f601-141">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1f601-141">**File**</span></span>|<span data-ttu-id="1f601-142">**Function**</span><span class="sxs-lookup"><span data-stu-id="1f601-142">**Function**</span></span>|<span data-ttu-id="1f601-143">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1f601-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f601-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="1f601-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="1f601-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="1f601-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="1f601-146">MFCMAPI usa o método **IMAPISession::OpenAddressBook** para obter o catálogo de endereços integrada.</span><span class="sxs-lookup"><span data-stu-id="1f601-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f601-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f601-147">See also</span></span>



[<span data-ttu-id="1f601-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1f601-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="1f601-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1f601-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="1f601-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="1f601-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="1f601-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f601-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1f601-152">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1f601-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

