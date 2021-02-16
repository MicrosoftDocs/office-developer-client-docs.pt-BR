---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428876"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="a228c-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a228c-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="a228c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a228c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a228c-105">Acessa recursos em um objeto de logon do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a228c-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a228c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a228c-106">Header file:</span></span>  <br/> |<span data-ttu-id="a228c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a228c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a228c-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="a228c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a228c-109">Objetos de logon do armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="a228c-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="a228c-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a228c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a228c-111">Provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="a228c-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="a228c-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a228c-112">Called by:</span></span>  <br/> |<span data-ttu-id="a228c-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="a228c-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="a228c-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a228c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a228c-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="a228c-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="a228c-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a228c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a228c-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="a228c-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a228c-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="a228c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a228c-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a228c-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="a228c-120">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a228c-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="a228c-121">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="a228c-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="a228c-122">Faz o login de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a228c-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="a228c-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a228c-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="a228c-124">Abre uma pasta ou objeto message e retorna um ponteiro para o objeto para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="a228c-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="a228c-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a228c-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="a228c-126">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="a228c-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="a228c-127">Advise</span><span class="sxs-lookup"><span data-stu-id="a228c-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="a228c-128">Registra um objeto com um provedor de armazenamento de mensagens para notificações sobre alterações no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a228c-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="a228c-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="a228c-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="a228c-130">Remove o registro de um objeto para notificação de alterações do armazenamento de mensagens estabelecidas anteriormente usando uma chamada para o **método IMSLogon::Advise.**</span><span class="sxs-lookup"><span data-stu-id="a228c-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="a228c-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a228c-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="a228c-132">Abre um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="a228c-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a228c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a228c-133">Remarks</span></span>

<span data-ttu-id="a228c-134">O objeto de logon do armazenamento de mensagens é a parte de um provedor de armazenamento de mensagens aberto que o MAPI chama diretamente.</span><span class="sxs-lookup"><span data-stu-id="a228c-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="a228c-135">Há uma correspondência um-para-um entre o objeto de logon do armazenamento de mensagens que o MAPI chama e o objeto de armazenamento de mensagens que os aplicativos cliente chamam; você pode pensar no logon e armazenar objetos como um objeto que expõe duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="a228c-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="a228c-136">Os dois objetos são criados juntos e liberados juntos.</span><span class="sxs-lookup"><span data-stu-id="a228c-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a228c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a228c-137">See also</span></span>



[<span data-ttu-id="a228c-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a228c-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

