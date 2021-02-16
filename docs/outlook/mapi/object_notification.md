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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430165"
---
# <a name="object_notification"></a><span data-ttu-id="c03b3-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="c03b3-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="c03b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c03b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c03b3-105">Contém informações sobre um objeto que passou por uma alteração, como sendo copiado ou modificado.</span><span class="sxs-lookup"><span data-stu-id="c03b3-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c03b3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c03b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c03b3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c03b3-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c03b3-108">Members</span><span class="sxs-lookup"><span data-stu-id="c03b3-108">Members</span></span>

 <span data-ttu-id="c03b3-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="c03b3-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID.**</span><span class="sxs-lookup"><span data-stu-id="c03b3-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="c03b3-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="c03b3-112">Ponteiro para o identificador de entrada do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="c03b3-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="c03b3-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="c03b3-113">**ulObjType**</span></span>
  
> <span data-ttu-id="c03b3-114">Tipo de objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="c03b3-114">Type of object affected.</span></span> <span data-ttu-id="c03b3-115">Os tipos possíveis são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="c03b3-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="c03b3-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="c03b3-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="c03b3-117">Armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c03b3-117">Message store.</span></span> 
    
<span data-ttu-id="c03b3-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="c03b3-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="c03b3-119">Address book.</span><span class="sxs-lookup"><span data-stu-id="c03b3-119">Address book.</span></span> 
    
<span data-ttu-id="c03b3-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="c03b3-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="c03b3-121">Pasta.</span><span class="sxs-lookup"><span data-stu-id="c03b3-121">Folder.</span></span>
    
<span data-ttu-id="c03b3-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="c03b3-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="c03b3-123">Contêiner do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="c03b3-123">Address book container.</span></span>
    
<span data-ttu-id="c03b3-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="c03b3-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="c03b3-125">Mensagem.</span><span class="sxs-lookup"><span data-stu-id="c03b3-125">Message.</span></span>
    
<span data-ttu-id="c03b3-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="c03b3-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="c03b3-127">Usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c03b3-127">Messaging user.</span></span>
    
<span data-ttu-id="c03b3-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="c03b3-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="c03b3-129">Anexo.</span><span class="sxs-lookup"><span data-stu-id="c03b3-129">Attachment.</span></span>
    
<span data-ttu-id="c03b3-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="c03b3-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="c03b3-131">Lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="c03b3-131">Distribution list.</span></span>
    
<span data-ttu-id="c03b3-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="c03b3-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="c03b3-133">Seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="c03b3-133">Profile section.</span></span>
    
<span data-ttu-id="c03b3-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="c03b3-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="c03b3-135">Objeto Status.</span><span class="sxs-lookup"><span data-stu-id="c03b3-135">Status object.</span></span>
    
<span data-ttu-id="c03b3-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="c03b3-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="c03b3-137">Objeto Session.</span><span class="sxs-lookup"><span data-stu-id="c03b3-137">Session object.</span></span>
    
 <span data-ttu-id="c03b3-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-138">**cbParentID**</span></span>
  
> <span data-ttu-id="c03b3-139">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID.**</span><span class="sxs-lookup"><span data-stu-id="c03b3-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="c03b3-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-140">**lpParentID**</span></span>
  
> <span data-ttu-id="c03b3-141">Ponteiro para o identificador de entrada do pai do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="c03b3-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="c03b3-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-142">**cbOldID**</span></span>
  
> <span data-ttu-id="c03b3-143">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldID.**</span><span class="sxs-lookup"><span data-stu-id="c03b3-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="c03b3-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-144">**lpOldID**</span></span>
  
> <span data-ttu-id="c03b3-145">Ponteiro para o identificador de entrada do objeto original.</span><span class="sxs-lookup"><span data-stu-id="c03b3-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="c03b3-146">Esse ponteiro poderá ser NULL se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="c03b3-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c03b3-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="c03b3-148">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldParentID.**</span><span class="sxs-lookup"><span data-stu-id="c03b3-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="c03b3-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="c03b3-150">Ponteiro para o identificador de entrada do pai do objeto original.</span><span class="sxs-lookup"><span data-stu-id="c03b3-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="c03b3-151">Esse ponteiro poderá ser NULL se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="c03b3-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="c03b3-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="c03b3-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="c03b3-153">Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém as marcas de propriedade que identificam as propriedades afetadas pelo evento.</span><span class="sxs-lookup"><span data-stu-id="c03b3-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c03b3-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="c03b3-154">Remarks</span></span>

<span data-ttu-id="c03b3-155">A **OBJECT_NOTIFICATION** estrutura é um dos membros da união de estruturas incluídas no membro **info** da estrutura [NOTIFICATION.](notification.md)</span><span class="sxs-lookup"><span data-stu-id="c03b3-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="c03b3-156">Quando o **membro de** informações de uma estrutura **NOTIFICATION** contém uma estrutura **OBJECT_NOTIFICATION,** o membro **ulEventType** da estrutura **NOTIFICATION** é definido como um dos seguintes tipos de eventos:</span><span class="sxs-lookup"><span data-stu-id="c03b3-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="c03b3-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="c03b3-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="c03b3-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="c03b3-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="c03b3-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="c03b3-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="c03b3-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="c03b3-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="c03b3-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="c03b3-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="c03b3-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="c03b3-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="c03b3-163">O evento de pesquisa completa, representado pelo tipo de evento fnevSearchComplete, indica que a pesquisa inicial do domínio para uma pasta de pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="c03b3-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="c03b3-164">Os membros a seguir que contêm informações sobre o objeto original são usados somente em eventos de movimentação e cópia.</span><span class="sxs-lookup"><span data-stu-id="c03b3-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="c03b3-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-165">**cbOldID**</span></span>
    
- <span data-ttu-id="c03b3-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-166">**lpOldID**</span></span>
    
- <span data-ttu-id="c03b3-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="c03b3-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="c03b3-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="c03b3-169">Esses membros não se aplicam aos outros tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="c03b3-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="c03b3-170">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c03b3-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="c03b3-171">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="c03b3-171">**Topic**</span></span>|<span data-ttu-id="c03b3-172">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c03b3-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c03b3-173">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="c03b3-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="c03b3-174">Visão geral dos eventos de notificação e notificação.</span><span class="sxs-lookup"><span data-stu-id="c03b3-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="c03b3-175">Manipulando notificações</span><span class="sxs-lookup"><span data-stu-id="c03b3-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="c03b3-176">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="c03b3-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="c03b3-177">Suporte à notificação de evento</span><span class="sxs-lookup"><span data-stu-id="c03b3-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="c03b3-178">Discussão sobre como os provedores de serviços podem usar o [método IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="c03b3-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c03b3-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="c03b3-179">See also</span></span>



[<span data-ttu-id="c03b3-180">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="c03b3-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="c03b3-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c03b3-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="c03b3-182">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c03b3-182">MAPI Structures</span></span>](mapi-structures.md)

