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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766891"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="b87b9-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="b87b9-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="b87b9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b87b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b87b9-105">Cancela um registro de notificação que tenha estabelecido para uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b87b9-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="b87b9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="b87b9-106">Parameters</span></span>

 <span data-ttu-id="b87b9-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="b87b9-107">_ulConnection_</span></span>
  
> <span data-ttu-id="b87b9-108">[in] Um número de conexão que representa o registro a ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="b87b9-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="b87b9-109">O parâmetro _ulConnection_ deve conter um valor retornado por uma chamada anterior para o método [IAddrBook::Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="b87b9-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b87b9-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b87b9-110">Return value</span></span>

<span data-ttu-id="b87b9-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b87b9-111">S_OK</span></span> 
  
> <span data-ttu-id="b87b9-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b87b9-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b87b9-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b87b9-113">Remarks</span></span>

<span data-ttu-id="b87b9-114">Clientes chame o método de **Unadvise** para parar de receber notificações sobre alterações em uma entrada de catálogo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="b87b9-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="b87b9-115">Quando um registro de notificação for cancelado, as versões de provedor de catálogo de endereços seu ponteiro para o chamador do coletor de eventos de aviso.</span><span class="sxs-lookup"><span data-stu-id="b87b9-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="b87b9-116">No entanto, a versão pode ocorrer durante a chamada **Unadvise** ou em algum momento posterior, se outro thread no processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="b87b9-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="b87b9-117">Quando uma notificação estiver em andamento, a versão foi adiada até que o método **OnNotify** retorna.</span><span class="sxs-lookup"><span data-stu-id="b87b9-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b87b9-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b87b9-118">See also</span></span>



[<span data-ttu-id="b87b9-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="b87b9-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="b87b9-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="b87b9-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="b87b9-121">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b87b9-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

