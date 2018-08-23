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
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563937"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="9d812-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d812-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="9d812-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d812-105">Recursos de acessos em uma mensagem armazenam o objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="9d812-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d812-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9d812-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d812-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="9d812-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9d812-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="9d812-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9d812-109">Objetos de logon do repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="9d812-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="9d812-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9d812-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d812-111">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="9d812-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="9d812-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9d812-112">Called by:</span></span>  <br/> |<span data-ttu-id="9d812-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d812-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d812-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9d812-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9d812-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="9d812-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="9d812-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="9d812-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9d812-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="9d812-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9d812-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="9d812-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9d812-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9d812-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="9d812-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d812-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="9d812-121">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="9d812-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="9d812-122">Logs de uma mensagem armazenam provedor.</span><span class="sxs-lookup"><span data-stu-id="9d812-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="9d812-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9d812-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="9d812-124">Abre uma pasta ou um objeto de mensagem e retorna um ponteiro para o objeto para fornecer mais acesso.</span><span class="sxs-lookup"><span data-stu-id="9d812-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="9d812-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9d812-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="9d812-126">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="9d812-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="9d812-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="9d812-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="9d812-128">Registra um objeto com um provedor de armazenamento de mensagem para notificações sobre alterações no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="9d812-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="9d812-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="9d812-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="9d812-130">Remove o registro de um objeto de notificação de alteração de repositório de mensagem tenha estabelecido por meio de uma chamada ao método **IMSLogon::Advise** .</span><span class="sxs-lookup"><span data-stu-id="9d812-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="9d812-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="9d812-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="9d812-132">Abre um objeto de status.</span><span class="sxs-lookup"><span data-stu-id="9d812-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d812-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d812-133">Remarks</span></span>

<span data-ttu-id="9d812-134">O objeto de logon do repositório de mensagens é a parte de um provedor de armazenamento de mensagem aberta diretamente chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d812-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="9d812-135">Não há uma correspondência direta entre o objeto de logon de armazenamento de mensagem que armazenam o objeto que aplicativos de cliente chamam; chamadas MAPI e a mensagem Você pode imaginar o logon e armazenar objetos como um único objeto que expõe duas interfaces.</span><span class="sxs-lookup"><span data-stu-id="9d812-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="9d812-136">Os dois objetos são criados juntos e liberação juntos.</span><span class="sxs-lookup"><span data-stu-id="9d812-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d812-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d812-137">See also</span></span>



[<span data-ttu-id="9d812-138">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9d812-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

