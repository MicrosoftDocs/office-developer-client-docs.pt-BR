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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416878"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="1cdd9-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="1cdd9-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="1cdd9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cdd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cdd9-105">Fornece acesso ao livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="1cdd9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cdd9-106">Parameters</span></span>

 <span data-ttu-id="1cdd9-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1cdd9-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1cdd9-108">[in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="1cdd9-109">Os valores válidos são NULL, que indica a interface padrão do livro de endereços [IAddrBook](iaddrbookimapiprop.md)e IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="1cdd9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1cdd9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1cdd9-111">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1cdd9-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="1cdd9-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="1cdd9-113">[out] Um ponteiro para um ponteiro para o livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1cdd9-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1cdd9-114">Return value</span></span>

<span data-ttu-id="1cdd9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cdd9-115">S_OK</span></span> 
  
> <span data-ttu-id="1cdd9-116">O acesso ao livro de endereços foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="1cdd9-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1cdd9-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1cdd9-118">A chamada foi bem-sucedida, mas não foi possível carregar um ou mais provedores de agendamento de endereços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="1cdd9-119">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="1cdd9-120">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="1cdd9-121">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="1cdd9-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1cdd9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cdd9-122">Remarks</span></span>

<span data-ttu-id="1cdd9-123">O **método IMAPISupport::OpenAddressBook** é implementado para todos os objetos de suporte do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="1cdd9-124">Os provedores de serviços, normalmente bem próximos de provedores de transporte e de armazenamento de mensagens, chamam **OpenAddressBook** para obter acesso ao livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="1cdd9-125">O ponteiro **IAddrBook** retornado pode ser usado para uma variedade de tarefas do livro de endereços, incluindo a abertura de contêineres do livro de endereços, a busca de usuários de mensagens e a exibição de caixas de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1cdd9-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1cdd9-126">Notes to callers</span></span>

 <span data-ttu-id="1cdd9-127">**OpenAddressBook** poderá retornar MAPI_W_ERRORS_RETURNED se não puder carregar um ou mais provedores de agendas no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="1cdd9-128">Esse valor é um aviso e você deve tratar a chamada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="1cdd9-129">Mesmo se todos os provedores de agendamento de endereços falharem ao carregar, **OpenAddressBook** ainda terá êxito, retornando MAPI_W_ERRORS_RETURNED e um ponteiro **IAddrBook** no parâmetro _lppAdrBook._</span><span class="sxs-lookup"><span data-stu-id="1cdd9-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="1cdd9-130">Como **OpenAddressBook** sempre retorna um ponteiro **IAddrBook** válido, você deve liberá-lo quando terminar de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="1cdd9-131">Se um ou mais provedores de agendamento de endereços falharem ao carregar, chame [IMAPISupport::GetLastError](imapisupport-getlasterror.md) para obter uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre os provedores que não foram carregados.</span><span class="sxs-lookup"><span data-stu-id="1cdd9-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1cdd9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cdd9-132">See also</span></span>



[<span data-ttu-id="1cdd9-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1cdd9-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="1cdd9-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="1cdd9-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="1cdd9-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1cdd9-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

