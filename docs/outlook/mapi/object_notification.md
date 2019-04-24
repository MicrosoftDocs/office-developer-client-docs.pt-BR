---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279883"
---
# <a name="objectnotification"></a><span data-ttu-id="106dd-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="106dd-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="106dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="106dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="106dd-105">Contém informações sobre um objeto que passou por uma alteração, como copiado ou modificado.</span><span class="sxs-lookup"><span data-stu-id="106dd-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="106dd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="106dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="106dd-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="106dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="106dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="106dd-108">Members</span></span>

 <span data-ttu-id="106dd-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="106dd-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="106dd-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="106dd-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="106dd-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="106dd-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="106dd-112">Ponteiro para o identificador de entrada do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="106dd-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="106dd-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="106dd-113">**ulObjType**</span></span>
  
> <span data-ttu-id="106dd-114">Tipo de objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="106dd-114">Type of object affected.</span></span> <span data-ttu-id="106dd-115">Os tipos possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="106dd-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="106dd-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="106dd-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="106dd-117">Repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="106dd-117">Message store.</span></span> 
    
<span data-ttu-id="106dd-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="106dd-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="106dd-119">Catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="106dd-119">Address book.</span></span> 
    
<span data-ttu-id="106dd-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="106dd-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="106dd-121">Ela.</span><span class="sxs-lookup"><span data-stu-id="106dd-121">Folder.</span></span>
    
<span data-ttu-id="106dd-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="106dd-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="106dd-123">Contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="106dd-123">Address book container.</span></span>
    
<span data-ttu-id="106dd-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="106dd-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="106dd-125">Mensagem.</span><span class="sxs-lookup"><span data-stu-id="106dd-125">Message.</span></span>
    
<span data-ttu-id="106dd-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="106dd-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="106dd-127">Usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="106dd-127">Messaging user.</span></span>
    
<span data-ttu-id="106dd-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="106dd-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="106dd-129">Anexar.</span><span class="sxs-lookup"><span data-stu-id="106dd-129">Attachment.</span></span>
    
<span data-ttu-id="106dd-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="106dd-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="106dd-131">Lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="106dd-131">Distribution list.</span></span>
    
<span data-ttu-id="106dd-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="106dd-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="106dd-133">Seção Profile.</span><span class="sxs-lookup"><span data-stu-id="106dd-133">Profile section.</span></span>
    
<span data-ttu-id="106dd-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="106dd-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="106dd-135">Objeto status.</span><span class="sxs-lookup"><span data-stu-id="106dd-135">Status object.</span></span>
    
<span data-ttu-id="106dd-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="106dd-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="106dd-137">Objeto Session.</span><span class="sxs-lookup"><span data-stu-id="106dd-137">Session object.</span></span>
    
 <span data-ttu-id="106dd-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-138">**cbParentID**</span></span>
  
> <span data-ttu-id="106dd-139">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="106dd-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="106dd-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-140">**lpParentID**</span></span>
  
> <span data-ttu-id="106dd-141">Ponteiro para o identificador de entrada do pai do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="106dd-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="106dd-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="106dd-142">**cbOldID**</span></span>
  
> <span data-ttu-id="106dd-143">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="106dd-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="106dd-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="106dd-144">**lpOldID**</span></span>
  
> <span data-ttu-id="106dd-145">Ponteiro para o identificador de entrada do objeto original.</span><span class="sxs-lookup"><span data-stu-id="106dd-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="106dd-146">Esse ponteiro pode ser nulo se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="106dd-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="106dd-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="106dd-148">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="106dd-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="106dd-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="106dd-150">Ponteiro para o identificador de entrada do pai do objeto original.</span><span class="sxs-lookup"><span data-stu-id="106dd-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="106dd-151">Esse ponteiro pode ser nulo se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="106dd-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="106dd-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="106dd-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="106dd-153">Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade identificando as propriedades afetadas pelo evento.</span><span class="sxs-lookup"><span data-stu-id="106dd-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="106dd-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="106dd-154">Remarks</span></span>

<span data-ttu-id="106dd-155">A estrutura **OBJECT_NOTIFICATION** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="106dd-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="106dd-156">Quando o membro **info** de uma estrutura de **notificação** contém uma estrutura **OBJECT_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como um dos seguintes tipos de eventos:</span><span class="sxs-lookup"><span data-stu-id="106dd-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="106dd-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="106dd-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="106dd-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="106dd-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="106dd-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="106dd-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="106dd-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="106dd-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="106dd-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="106dd-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="106dd-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="106dd-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="106dd-163">O evento Search Complete, representado pelo tipo de evento fnevSearchComplete, indica que a pesquisa inicial do domínio de uma pasta de pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="106dd-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="106dd-164">Os membros a seguir que contêm informações sobre o objeto original são usados somente nos eventos mover e copiar.</span><span class="sxs-lookup"><span data-stu-id="106dd-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="106dd-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="106dd-165">**cbOldID**</span></span>
    
- <span data-ttu-id="106dd-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="106dd-166">**lpOldID**</span></span>
    
- <span data-ttu-id="106dd-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="106dd-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="106dd-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="106dd-169">Esses membros não se aplicam aos outros tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="106dd-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="106dd-170">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="106dd-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="106dd-171">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="106dd-171">**Topic**</span></span>|<span data-ttu-id="106dd-172">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="106dd-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="106dd-173">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="106dd-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="106dd-174">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="106dd-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="106dd-175">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="106dd-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="106dd-176">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="106dd-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="106dd-177">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="106dd-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="106dd-178">Discussão sobre como os provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="106dd-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="106dd-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="106dd-179">See also</span></span>



[<span data-ttu-id="106dd-180">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="106dd-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="106dd-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="106dd-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="106dd-182">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="106dd-182">MAPI Structures</span></span>](mapi-structures.md)

