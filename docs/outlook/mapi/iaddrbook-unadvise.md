---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436150"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="ce240-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ce240-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="ce240-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce240-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce240-105">Cancela um registro de notificação estabelecido previamente para uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ce240-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ce240-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce240-106">Parameters</span></span>

 <span data-ttu-id="ce240-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ce240-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ce240-108">no Um número de conexão que representa o registro a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="ce240-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="ce240-109">O parâmetro _ulConnection_ deve conter um valor retornado por uma chamada anterior para o método [IAddrBook:: Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="ce240-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce240-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ce240-110">Return value</span></span>

<span data-ttu-id="ce240-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce240-111">S_OK</span></span> 
  
> <span data-ttu-id="ce240-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="ce240-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce240-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce240-113">Remarks</span></span>

<span data-ttu-id="ce240-114">Os clientes chamam o método **Unadvise** para parar de receber notificações sobre alterações em uma entrada de catálogo de endereços específica.</span><span class="sxs-lookup"><span data-stu-id="ce240-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="ce240-115">Quando um registro de notificação é cancelado, o provedor de catálogo de endereços libera o ponteiro para o coletor de aviso do chamador.</span><span class="sxs-lookup"><span data-stu-id="ce240-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="ce240-116">No enTanto, o lançamento pode ocorrer durante a chamada a **Unadvise** ou, posteriormente, se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce240-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="ce240-117">Quando uma notificação estiver em andamento, a versão será atrasada até o \*\*\*\* método OnNotify retornar.</span><span class="sxs-lookup"><span data-stu-id="ce240-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce240-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce240-118">See also</span></span>



[<span data-ttu-id="ce240-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="ce240-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="ce240-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ce240-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ce240-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ce240-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

