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
# <a name="iaddrbookunadvise"></a><span data-ttu-id="d3308-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="d3308-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="d3308-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3308-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3308-105">Cancela um registro de notificação estabelecido anteriormente para uma entrada do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="d3308-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d3308-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3308-106">Parameters</span></span>

 <span data-ttu-id="d3308-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="d3308-107">_ulConnection_</span></span>
  
> <span data-ttu-id="d3308-108">[in] Um número de conexão que representa o registro a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="d3308-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="d3308-109">O _parâmetro ulConnection_ deve conter um valor retornado por uma chamada anterior para o [método IAddrBook::Advise.](iaddrbook-advise.md)</span><span class="sxs-lookup"><span data-stu-id="d3308-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d3308-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d3308-110">Return value</span></span>

<span data-ttu-id="d3308-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3308-111">S_OK</span></span> 
  
> <span data-ttu-id="d3308-112">O registro foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d3308-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3308-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3308-113">Remarks</span></span>

<span data-ttu-id="d3308-114">Os clientes chamam **o método Unadvise** para parar de receber notificações sobre alterações em uma entrada específica do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="d3308-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="d3308-115">Quando um registro de notificação é cancelado, o provedor de agendamento libera seu ponteiro para o pia de aviso do chamador.</span><span class="sxs-lookup"><span data-stu-id="d3308-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="d3308-116">No entanto, a versão pode ocorrer durante a chamada **Unadvise** ou em algum momento posterior, se outro thread estiver em processo de chamada do método [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="d3308-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="d3308-117">Quando uma notificação está em andamento, a versão é adiada até que o **método OnNotify** retorne.</span><span class="sxs-lookup"><span data-stu-id="d3308-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3308-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3308-118">See also</span></span>



[<span data-ttu-id="d3308-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="d3308-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="d3308-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d3308-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d3308-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d3308-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

