---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d427adde72c24d4ca879c7bd883af09c4ecad53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579967"
---
# <a name="notification"></a><span data-ttu-id="d2234-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-103">NOTIFICATION</span></span>
 
<span data-ttu-id="d2234-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2234-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2234-105">Contém informações sobre um evento que ocorreu e os dados que foi afetados pelo evento.</span><span class="sxs-lookup"><span data-stu-id="d2234-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2234-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d2234-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2234-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2234-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="d2234-108">Members</span><span class="sxs-lookup"><span data-stu-id="d2234-108">Members</span></span>

<span data-ttu-id="d2234-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="d2234-109">**ulEventType**</span></span>
  
> <span data-ttu-id="d2234-110">Tipo de evento de notificação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d2234-110">Type of notification event that occurred.</span></span> <span data-ttu-id="d2234-111">O valor do membro **ulEventType** corresponde à estrutura que está incluída na União **info** .</span><span class="sxs-lookup"><span data-stu-id="d2234-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="d2234-112">O membro **ulEventType** pode ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d2234-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="d2234-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="d2234-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="d2234-114">Ocorreu um erro global, como uma sessão desligar em andamento.</span><span class="sxs-lookup"><span data-stu-id="d2234-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="d2234-115">O membro **info** contém uma estrutura [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d2234-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2234-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="d2234-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="d2234-117">Ocorreu um evento interno definido por um provedor de serviço específico.</span><span class="sxs-lookup"><span data-stu-id="d2234-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="d2234-118">O membro **info** contém uma estrutura [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d2234-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2234-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="d2234-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="d2234-120">Uma mensagem foi entregue ao receber a pasta para a classe de mensagem e está aguardando processamento apropriada.</span><span class="sxs-lookup"><span data-stu-id="d2234-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="d2234-121">O membro **info** contém uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d2234-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2234-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="d2234-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="d2234-123">Um objeto MAPI foi copiado.</span><span class="sxs-lookup"><span data-stu-id="d2234-123">A MAPI object has been copied.</span></span> <span data-ttu-id="d2234-124">O membro **info** contém uma estrutura [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d2234-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="d2234-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="d2234-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="d2234-126">Um objeto MAPI foi criado.</span><span class="sxs-lookup"><span data-stu-id="d2234-126">A MAPI object has been created.</span></span> <span data-ttu-id="d2234-127">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="d2234-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2234-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="d2234-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="d2234-129">Um objeto MAPI foi excluído.</span><span class="sxs-lookup"><span data-stu-id="d2234-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="d2234-130">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="d2234-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2234-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="d2234-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="d2234-132">Um objeto MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d2234-132">A MAPI object has changed.</span></span> <span data-ttu-id="d2234-133">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="d2234-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2234-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="d2234-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="d2234-135">Um armazenamento de mensagens ou endereço livro objeto tiver sido movido.</span><span class="sxs-lookup"><span data-stu-id="d2234-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="d2234-136">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="d2234-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2234-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="d2234-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="d2234-138">Uma operação de pesquisa foi concluída e os resultados estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="d2234-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="d2234-139">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="d2234-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="d2234-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="d2234-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="d2234-141">Informações em uma tabela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="d2234-141">Information in a table has changed.</span></span> <span data-ttu-id="d2234-142">O membro **info** contém uma estrutura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="d2234-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="d2234-143">**Info**</span><span class="sxs-lookup"><span data-stu-id="d2234-143">**info**</span></span>
  
> <span data-ttu-id="d2234-144">União de estruturas de notificação descrevendo os dados afetados para um determinado tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="d2234-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="d2234-145">A estrutura incluída no membro **info** depende do valor do membro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="d2234-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2234-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2234-146">Remarks</span></span>

<span data-ttu-id="d2234-147">Uma ou mais estruturas de **notificação** são passadas como parâmetros de entrada com cada chamada ao método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) um advise registrados do receptor.</span><span class="sxs-lookup"><span data-stu-id="d2234-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="d2234-148">As estruturas de **notificação** contêm informações sobre as determinados eventos ocorridos e descrevem os objetos afetados.</span><span class="sxs-lookup"><span data-stu-id="d2234-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="d2234-149">Antes de clientes ou receber uma notificação de provedores de serviços podem usar a estrutura para processar o evento, eles devem verificar o tipo de evento, conforme indicado no membro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="d2234-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="d2234-150">Por exemplo, o exemplo de código que é mostrado aqui verifica a chegada de uma nova mensagem e ao detectar um evento desse tipo, imprime a classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2234-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="d2234-151">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2234-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="d2234-152">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="d2234-152">**Topic**</span></span>|<span data-ttu-id="d2234-153">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d2234-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2234-154">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="d2234-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="d2234-155">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="d2234-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="d2234-156">Lidar com notificações</span><span class="sxs-lookup"><span data-stu-id="d2234-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="d2234-157">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="d2234-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="d2234-158">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="d2234-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="d2234-159">Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="d2234-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2234-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2234-160">See also</span></span>


- [<span data-ttu-id="d2234-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="d2234-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="d2234-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="d2234-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="d2234-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="d2234-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d2234-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="d2234-167">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="d2234-167">MAPI Structures</span></span>](mapi-structures.md)

