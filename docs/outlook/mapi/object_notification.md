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
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768168"
---
# <a name="objectnotification"></a><span data-ttu-id="78ab0-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="78ab0-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="78ab0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78ab0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78ab0-105">Contém informações sobre um objeto que sofreram uma alteração, tais como sendo copiado ou modificado.</span><span class="sxs-lookup"><span data-stu-id="78ab0-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78ab0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="78ab0-106">Header file:</span></span>  <br/> |<span data-ttu-id="78ab0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="78ab0-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="78ab0-108">Members</span><span class="sxs-lookup"><span data-stu-id="78ab0-108">Members</span></span>

 <span data-ttu-id="78ab0-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="78ab0-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="78ab0-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="78ab0-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="78ab0-112">Ponteiro para o identificador de entrada do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="78ab0-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="78ab0-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="78ab0-113">**ulObjType**</span></span>
  
> <span data-ttu-id="78ab0-114">Tipo de objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="78ab0-114">Type of object affected.</span></span> <span data-ttu-id="78ab0-115">Os tipos possíveis são:</span><span class="sxs-lookup"><span data-stu-id="78ab0-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="78ab0-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="78ab0-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="78ab0-117">Armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="78ab0-117">Message store.</span></span> 
    
<span data-ttu-id="78ab0-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="78ab0-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="78ab0-119">Catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="78ab0-119">Address book.</span></span> 
    
<span data-ttu-id="78ab0-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="78ab0-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="78ab0-121">Pasta.</span><span class="sxs-lookup"><span data-stu-id="78ab0-121">Folder.</span></span>
    
<span data-ttu-id="78ab0-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="78ab0-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="78ab0-123">Contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="78ab0-123">Address book container.</span></span>
    
<span data-ttu-id="78ab0-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="78ab0-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="78ab0-125">Mensagem.</span><span class="sxs-lookup"><span data-stu-id="78ab0-125">Message.</span></span>
    
<span data-ttu-id="78ab0-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="78ab0-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="78ab0-127">Usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="78ab0-127">Messaging user.</span></span>
    
<span data-ttu-id="78ab0-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="78ab0-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="78ab0-129">Anexo.</span><span class="sxs-lookup"><span data-stu-id="78ab0-129">Attachment.</span></span>
    
<span data-ttu-id="78ab0-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="78ab0-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="78ab0-131">Lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="78ab0-131">Distribution list.</span></span>
    
<span data-ttu-id="78ab0-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="78ab0-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="78ab0-133">Seção de perfil.</span><span class="sxs-lookup"><span data-stu-id="78ab0-133">Profile section.</span></span>
    
<span data-ttu-id="78ab0-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="78ab0-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="78ab0-135">Objeto de status.</span><span class="sxs-lookup"><span data-stu-id="78ab0-135">Status object.</span></span>
    
<span data-ttu-id="78ab0-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="78ab0-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="78ab0-137">Objeto da sessão.</span><span class="sxs-lookup"><span data-stu-id="78ab0-137">Session object.</span></span>
    
 <span data-ttu-id="78ab0-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-138">**cbParentID**</span></span>
  
> <span data-ttu-id="78ab0-139">Contagem de bytes no identificador de entrada apontado pelo membro **lpParentID** .</span><span class="sxs-lookup"><span data-stu-id="78ab0-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="78ab0-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-140">**lpParentID**</span></span>
  
> <span data-ttu-id="78ab0-141">Ponteiro para o identificador de entrada do pai do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="78ab0-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="78ab0-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-142">**cbOldID**</span></span>
  
> <span data-ttu-id="78ab0-143">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldID** .</span><span class="sxs-lookup"><span data-stu-id="78ab0-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="78ab0-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-144">**lpOldID**</span></span>
  
> <span data-ttu-id="78ab0-145">Ponteiro para o identificador de entrada do objeto original.</span><span class="sxs-lookup"><span data-stu-id="78ab0-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="78ab0-146">Esse ponteiro pode ser NULL se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="78ab0-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="78ab0-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="78ab0-148">Contagem de bytes no identificador de entrada apontado pelo membro **lpOldParentID** .</span><span class="sxs-lookup"><span data-stu-id="78ab0-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="78ab0-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="78ab0-150">Ponteiro para o identificador de entrada do pai do objeto original.</span><span class="sxs-lookup"><span data-stu-id="78ab0-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="78ab0-151">Esse ponteiro pode ser NULL se o evento não exigir um objeto original.</span><span class="sxs-lookup"><span data-stu-id="78ab0-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="78ab0-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="78ab0-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="78ab0-153">Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém as marcas de propriedade identificando propriedades afetadas pelo evento.</span><span class="sxs-lookup"><span data-stu-id="78ab0-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="78ab0-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="78ab0-154">Remarks</span></span>

<span data-ttu-id="78ab0-155">A estrutura **OBJECT_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="78ab0-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="78ab0-156">Quando o membro de **informações** de uma estrutura de **notificação** contém uma estrutura **OBJECT_NOTIFICATION** , o membro **ulEventType** da estrutura de **notificação** é definido como um dos seguintes tipos de eventos:</span><span class="sxs-lookup"><span data-stu-id="78ab0-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="78ab0-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="78ab0-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="78ab0-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="78ab0-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="78ab0-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="78ab0-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="78ab0-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="78ab0-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="78ab0-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="78ab0-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="78ab0-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="78ab0-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="78ab0-163">O evento complete de pesquisa, representado pelo tipo de evento fnevSearchComplete, indica se a pesquisa inicial do domínio para a pasta de pesquisa de um foi concluída.</span><span class="sxs-lookup"><span data-stu-id="78ab0-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="78ab0-164">Os seguintes membros que contêm informações sobre o objeto original são usados somente nos eventos de mover e copiar.</span><span class="sxs-lookup"><span data-stu-id="78ab0-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="78ab0-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-165">**cbOldID**</span></span>
    
- <span data-ttu-id="78ab0-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-166">**lpOldID**</span></span>
    
- <span data-ttu-id="78ab0-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="78ab0-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="78ab0-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="78ab0-169">Esses membros não se aplicam aos outros tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="78ab0-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="78ab0-170">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="78ab0-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="78ab0-171">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="78ab0-171">**Topic**</span></span>|<span data-ttu-id="78ab0-172">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="78ab0-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78ab0-173">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="78ab0-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="78ab0-174">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="78ab0-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="78ab0-175">Lidar com notificações</span><span class="sxs-lookup"><span data-stu-id="78ab0-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="78ab0-176">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="78ab0-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="78ab0-177">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="78ab0-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="78ab0-178">Discussão sobre como provedores de serviços podem usar o método [IMAPISupport](imapisupportiunknown.md) para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="78ab0-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78ab0-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="78ab0-179">See also</span></span>



[<span data-ttu-id="78ab0-180">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="78ab0-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="78ab0-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="78ab0-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="78ab0-182">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="78ab0-182">MAPI Structures</span></span>](mapi-structures.md)

