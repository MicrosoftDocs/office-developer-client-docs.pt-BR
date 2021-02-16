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
# <a name="notification"></a><span data-ttu-id="c0be9-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-103">NOTIFICATION</span></span>
 
<span data-ttu-id="c0be9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0be9-105">Contém informações sobre um evento que ocorreu e os dados que foram afetados pelo evento.</span><span class="sxs-lookup"><span data-stu-id="c0be9-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0be9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c0be9-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0be9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0be9-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c0be9-108">Members</span><span class="sxs-lookup"><span data-stu-id="c0be9-108">Members</span></span>

<span data-ttu-id="c0be9-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="c0be9-109">**ulEventType**</span></span>
  
> <span data-ttu-id="c0be9-110">Tipo de evento de notificação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c0be9-110">Type of notification event that occurred.</span></span> <span data-ttu-id="c0be9-111">O valor do **membro ulEventType** corresponde à estrutura incluída na união **de** informações.</span><span class="sxs-lookup"><span data-stu-id="c0be9-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="c0be9-112">O **membro ulEventType** pode ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c0be9-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="c0be9-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="c0be9-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="c0be9-114">Ocorreu um erro global, como o desligar de uma sessão em andamento.</span><span class="sxs-lookup"><span data-stu-id="c0be9-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="c0be9-115">O **membro de** informações contém uma [ERROR_NOTIFICATION](error_notification.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c0be9-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="c0be9-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="c0be9-117">Ocorreu um evento interno definido por um provedor de serviços específico.</span><span class="sxs-lookup"><span data-stu-id="c0be9-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="c0be9-118">O **membro de** informações contém uma [EXTENDED_NOTIFICATION](extended_notification.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c0be9-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="c0be9-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="c0be9-120">Uma mensagem foi entregue à pasta de recebimento apropriada para a classe de mensagens e está aguardando para ser processada.</span><span class="sxs-lookup"><span data-stu-id="c0be9-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="c0be9-121">O **membro** de informações contém uma [NEWMAIL_NOTIFICATION](newmail_notification.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c0be9-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="c0be9-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="c0be9-123">Um objeto MAPI foi copiado.</span><span class="sxs-lookup"><span data-stu-id="c0be9-123">A MAPI object has been copied.</span></span> <span data-ttu-id="c0be9-124">O **membro** de informações contém uma [OBJECT_NOTIFICATION](object_notification.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="c0be9-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="c0be9-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="c0be9-126">Um objeto MAPI foi criado.</span><span class="sxs-lookup"><span data-stu-id="c0be9-126">A MAPI object has been created.</span></span> <span data-ttu-id="c0be9-127">O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c0be9-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="c0be9-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="c0be9-129">Um objeto MAPI foi excluído.</span><span class="sxs-lookup"><span data-stu-id="c0be9-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="c0be9-130">O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c0be9-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="c0be9-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="c0be9-132">Um objeto MAPI foi alterado.</span><span class="sxs-lookup"><span data-stu-id="c0be9-132">A MAPI object has changed.</span></span> <span data-ttu-id="c0be9-133">O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c0be9-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="c0be9-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="c0be9-135">Um objeto de armazenamento de mensagens ou de um livro de endereços foi movido.</span><span class="sxs-lookup"><span data-stu-id="c0be9-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="c0be9-136">O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c0be9-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="c0be9-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="c0be9-138">Uma operação de pesquisa foi concluída e os resultados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c0be9-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="c0be9-139">O **membro** de informações contém uma **OBJECT_NOTIFICATION** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="c0be9-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="c0be9-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="c0be9-141">As informações em uma tabela foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="c0be9-141">Information in a table has changed.</span></span> <span data-ttu-id="c0be9-142">O **membro de** informações contém uma [TABLE_NOTIFICATION](table_notification.md) estrutura.</span><span class="sxs-lookup"><span data-stu-id="c0be9-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="c0be9-143">**informações**</span><span class="sxs-lookup"><span data-stu-id="c0be9-143">**info**</span></span>
  
> <span data-ttu-id="c0be9-144">União de estruturas de notificação que descrevem os dados afetados para um tipo específico de evento.</span><span class="sxs-lookup"><span data-stu-id="c0be9-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="c0be9-145">A estrutura incluída no membro **info** depende do valor do **membro ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="c0be9-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c0be9-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0be9-146">Remarks</span></span>

<span data-ttu-id="c0be9-147">Uma ou mais estruturas **notification** são passadas como parâmetros de entrada com cada chamada para o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de um pia de aviso registrado.</span><span class="sxs-lookup"><span data-stu-id="c0be9-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="c0be9-148">As **estruturas** NOTIFICATION contêm informações sobre os eventos específicos que ocorreram e descrevem os objetos afetados.</span><span class="sxs-lookup"><span data-stu-id="c0be9-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="c0be9-149">Antes que os clientes ou provedores de serviços que recebem uma notificação possam usar a estrutura para processar o evento, eles devem verificar o tipo de evento conforme indicado no **membro ulEventType.**</span><span class="sxs-lookup"><span data-stu-id="c0be9-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="c0be9-150">Por exemplo, o exemplo de código mostrado aqui verifica a chegada de uma nova mensagem e, ao detectar um evento desse tipo, imprime a classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c0be9-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="c0be9-151">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0be9-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c0be9-152">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="c0be9-152">**Topic**</span></span>|<span data-ttu-id="c0be9-153">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c0be9-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0be9-154">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="c0be9-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c0be9-155">Visão geral dos eventos de notificação e notificação.</span><span class="sxs-lookup"><span data-stu-id="c0be9-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c0be9-156">Manipulando notificações</span><span class="sxs-lookup"><span data-stu-id="c0be9-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c0be9-157">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="c0be9-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c0be9-158">Suporte à notificação de evento</span><span class="sxs-lookup"><span data-stu-id="c0be9-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c0be9-159">Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="c0be9-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0be9-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0be9-160">See also</span></span>


- [<span data-ttu-id="c0be9-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="c0be9-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="c0be9-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="c0be9-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="c0be9-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="c0be9-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c0be9-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="c0be9-167">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c0be9-167">MAPI Structures</span></span>](mapi-structures.md)

