---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e9cd1c7ce0983a47311b2626cc3b40b47748b951
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767266"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="b1a2f-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="b1a2f-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="b1a2f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1a2f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1a2f-105">Fornece acesso ao catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="b1a2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1a2f-106">Parameters</span></span>

 <span data-ttu-id="b1a2f-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b1a2f-107">_lpInterface_</span></span>
  
> <span data-ttu-id="b1a2f-108">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="b1a2f-109">Valores válidos são NULL, indicando que a interface de catálogo de endereços padrão [IAddrBook](iaddrbookimapiprop.md)e IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="b1a2f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1a2f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b1a2f-111">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b1a2f-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="b1a2f-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="b1a2f-113">[out] Um ponteiro para um ponteiro para o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1a2f-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1a2f-114">Return value</span></span>

<span data-ttu-id="b1a2f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1a2f-115">S_OK</span></span> 
  
> <span data-ttu-id="b1a2f-116">Acesso ao catálogo de endereços foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="b1a2f-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="b1a2f-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="b1a2f-118">A chamada foi bem-sucedida, mas um ou mais provedores de catálogo de endereços não pôde ser carregados.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="b1a2f-119">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b1a2f-120">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="b1a2f-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b1a2f-121">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="b1a2f-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1a2f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1a2f-122">Remarks</span></span>

<span data-ttu-id="b1a2f-123">O método **IMAPISupport::OpenAddressBook** é implementado para todos os objetos de suporte de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="b1a2f-124">Provedores de serviços de mensagem de ligação geralmente estreita armazenam e provedores de transporte, chame **OpenAddressBook** para obter acesso ao catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="b1a2f-125">O ponteiro **IAddrBook** retornado pode ser usado para uma variedade de tarefas do catálogo de endereços, incluindo a abertura de contêineres de catálogo de endereço, Localizando usuários mensagens e exibindo caixas de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1a2f-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b1a2f-126">Notes to callers</span></span>

 <span data-ttu-id="b1a2f-127">**OpenAddressBook** pode retornar MAPI_W_ERRORS_RETURNED se ele não é possível carregar um ou mais dos provedores de catálogo de endereços no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="b1a2f-128">Esse valor é um aviso e a chamada devem ser tratados como bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="b1a2f-129">Mesmo que todos os provedores de catálogo de endereços Falha ao carregar, **OpenAddressBook** ainda tiver êxito, retornando MAPI_W_ERRORS_RETURNED e um ponteiro **IAddrBook** no parâmetro _lppAdrBook_ .</span><span class="sxs-lookup"><span data-stu-id="b1a2f-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="b1a2f-130">Como **OpenAddressBook** sempre retorna um ponteiro **IAddrBook** válido, você deve liberá-lo quando terminar de utilizá-lo.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="b1a2f-131">Se um ou mais provedores de catálogo de endereços Falha ao carregar, chame [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores que não é carregado.</span><span class="sxs-lookup"><span data-stu-id="b1a2f-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1a2f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1a2f-132">See also</span></span>



[<span data-ttu-id="b1a2f-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b1a2f-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="b1a2f-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="b1a2f-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="b1a2f-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1a2f-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

