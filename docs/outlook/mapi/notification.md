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
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432874"
---
# <a name="notification"></a><span data-ttu-id="3e990-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-103">NOTIFICATION</span></span>
 
<span data-ttu-id="3e990-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e990-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e990-105">Contém informações sobre um evento que ocorreu e os dados afetados pelo evento.</span><span class="sxs-lookup"><span data-stu-id="3e990-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e990-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3e990-106">Header file:</span></span>  <br/> |<span data-ttu-id="3e990-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3e990-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="3e990-108">Members</span><span class="sxs-lookup"><span data-stu-id="3e990-108">Members</span></span>

<span data-ttu-id="3e990-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="3e990-109">**ulEventType**</span></span>
  
> <span data-ttu-id="3e990-110">Tipo de evento de notificação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="3e990-110">Type of notification event that occurred.</span></span> <span data-ttu-id="3e990-111">O valor do membro **ulEventType** corresponde à estrutura que está incluída na União **info** .</span><span class="sxs-lookup"><span data-stu-id="3e990-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="3e990-112">O membro **ulEventType** pode ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3e990-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="3e990-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="3e990-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="3e990-114">Ocorreu um erro global, como uma sessão desligada em andamento.</span><span class="sxs-lookup"><span data-stu-id="3e990-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="3e990-115">O membro **info** contém uma estrutura [ERROR_NOTIFICATION](error_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3e990-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="3e990-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="3e990-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="3e990-117">Um evento interno definido por um determinado provedor de serviços ocorreu.</span><span class="sxs-lookup"><span data-stu-id="3e990-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="3e990-118">O membro **info** contém uma estrutura [EXTENDED_NOTIFICATION](extended_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3e990-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="3e990-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="3e990-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="3e990-120">Uma mensagem foi entregue à pasta de recebimento apropriada para a classe de mensagem e está aguardando para ser processada.</span><span class="sxs-lookup"><span data-stu-id="3e990-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="3e990-121">O membro **info** contém uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3e990-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="3e990-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="3e990-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="3e990-123">Um objeto MAPI foi copiado.</span><span class="sxs-lookup"><span data-stu-id="3e990-123">A MAPI object has been copied.</span></span> <span data-ttu-id="3e990-124">O membro **info** contém uma estrutura [OBJECT_NOTIFICATION](object_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3e990-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="3e990-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="3e990-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="3e990-126">Um objeto MAPI foi criado.</span><span class="sxs-lookup"><span data-stu-id="3e990-126">A MAPI object has been created.</span></span> <span data-ttu-id="3e990-127">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="3e990-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="3e990-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="3e990-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="3e990-129">Um objeto MAPI foi excluído.</span><span class="sxs-lookup"><span data-stu-id="3e990-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="3e990-130">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="3e990-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="3e990-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="3e990-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="3e990-132">Um objeto MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3e990-132">A MAPI object has changed.</span></span> <span data-ttu-id="3e990-133">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="3e990-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="3e990-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="3e990-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="3e990-135">Um objeto de repositório de mensagens ou de catálogo de endereços foi movido.</span><span class="sxs-lookup"><span data-stu-id="3e990-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="3e990-136">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="3e990-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="3e990-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="3e990-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="3e990-138">Uma operação de pesquisa foi concluída e os resultados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3e990-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="3e990-139">O membro **info** contém uma estrutura **OBJECT_NOTIFICATION** .</span><span class="sxs-lookup"><span data-stu-id="3e990-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="3e990-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="3e990-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="3e990-141">As informações em uma tabela foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="3e990-141">Information in a table has changed.</span></span> <span data-ttu-id="3e990-142">O membro **info** contém uma estrutura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="3e990-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="3e990-143">\*\*informações \*\*</span><span class="sxs-lookup"><span data-stu-id="3e990-143">**info**</span></span>
  
> <span data-ttu-id="3e990-144">União de estruturas de notificação descrevendo os dados afetados para um tipo específico de evento.</span><span class="sxs-lookup"><span data-stu-id="3e990-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="3e990-145">A estrutura incluída no membro **info** depende do valor do membro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="3e990-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3e990-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e990-146">Remarks</span></span>

<span data-ttu-id="3e990-147">Uma ou mais estruturas de **notificação** são passadas como parâmetros de entrada com cada chamada para o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) de um coletor de aviso registrado.</span><span class="sxs-lookup"><span data-stu-id="3e990-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="3e990-148">As estruturas de **notificação** contêm informações sobre os eventos específicos que ocorreram e descrevem os objetos afetados.</span><span class="sxs-lookup"><span data-stu-id="3e990-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="3e990-149">Antes que os clientes ou provedores de serviços que recebem uma notificação podem usar a estrutura para processar o evento, eles devem verificar o tipo de evento conforme indicado no membro **ulEventType** .</span><span class="sxs-lookup"><span data-stu-id="3e990-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="3e990-150">Por exemplo, o exemplo de código mostrado aqui verifica a chegada de uma nova mensagem e, após detectar um evento desse tipo, imprime a classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="3e990-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="3e990-151">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e990-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="3e990-152">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="3e990-152">**Topic**</span></span>|<span data-ttu-id="3e990-153">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e990-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e990-154">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="3e990-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="3e990-155">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="3e990-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="3e990-156">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="3e990-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="3e990-157">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="3e990-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="3e990-158">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="3e990-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="3e990-159">Discussão sobre como os provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="3e990-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e990-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e990-160">See also</span></span>


- [<span data-ttu-id="3e990-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="3e990-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="3e990-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="3e990-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="3e990-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="3e990-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="3e990-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="3e990-167">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="3e990-167">MAPI Structures</span></span>](mapi-structures.md)

