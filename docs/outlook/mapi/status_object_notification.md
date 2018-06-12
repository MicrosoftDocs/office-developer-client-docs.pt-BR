---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 71e0a08436c925f0d68d63111722cc01bd73cc5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770517"
---
# <a name="statusobjectnotification"></a><span data-ttu-id="6b230-103">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="6b230-103">STATUS_OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="6b230-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b230-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b230-105">Descreve um objeto de status que tenha sido afetado por uma alteração.</span><span class="sxs-lookup"><span data-stu-id="6b230-105">Describes a status object that has been affected by a change.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b230-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6b230-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b230-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b230-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="6b230-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6b230-108">Members</span></span>

 <span data-ttu-id="6b230-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="6b230-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="6b230-110">Contagem de bytes no identificador de entrada apontado pelo membro **lpEntryID** .</span><span class="sxs-lookup"><span data-stu-id="6b230-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="6b230-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="6b230-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="6b230-112">Ponteiro para o identificador de entrada do objeto status alterado.</span><span class="sxs-lookup"><span data-stu-id="6b230-112">Pointer to the entry identifier of the changed status object.</span></span>
    
 <span data-ttu-id="6b230-113">**cValues**</span><span class="sxs-lookup"><span data-stu-id="6b230-113">**cValues**</span></span>
  
> <span data-ttu-id="6b230-114">Contagem de estruturas de [SPropValue](spropvalue.md) na matriz apontado pelo membro **lpPropVals** .</span><span class="sxs-lookup"><span data-stu-id="6b230-114">Count of [SPropValue](spropvalue.md) structures in the array pointed to by the **lpPropVals** member.</span></span> 
    
 <span data-ttu-id="6b230-115">**lpPropVals**</span><span class="sxs-lookup"><span data-stu-id="6b230-115">**lpPropVals**</span></span>
  
> <span data-ttu-id="6b230-116">Ponteiro para uma matriz de estruturas de **SPropValue** que descrevem as propriedades do objeto status alterado.</span><span class="sxs-lookup"><span data-stu-id="6b230-116">Pointer to an array of **SPropValue** structures that describe the properties of the changed status object.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b230-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="6b230-117">Remarks</span></span>

<span data-ttu-id="6b230-118">A estrutura **STATUS_OBJECT_NOTIFICATION** é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="6b230-118">The **STATUS_OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="6b230-119">A estrutura **STATUS_OBJECT_NOTIFICATION** está incluída com uma notificação de objeto de status para um evento do tipo _fnevStatusObjectModified_.</span><span class="sxs-lookup"><span data-stu-id="6b230-119">The **STATUS_OBJECT_NOTIFICATION** structure is included with a status object notification for an event of type  _fnevStatusObjectModified_.</span></span> <span data-ttu-id="6b230-120">Notificação de status de objeto é uma notificação de MAPI interna; clientes e provedores de serviços não é possível registrar para ele e provedores de serviços não é possível gerar a ele.</span><span class="sxs-lookup"><span data-stu-id="6b230-120">Status object notification is an internal MAPI notification; clients and service providers cannot register for it and service providers cannot generate it.</span></span>
  
<span data-ttu-id="6b230-121">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b230-121">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="6b230-122">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="6b230-122">**Topic**</span></span>|<span data-ttu-id="6b230-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6b230-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b230-124">Notificação de evento em MAPI</span><span class="sxs-lookup"><span data-stu-id="6b230-124">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="6b230-125">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="6b230-125">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="6b230-126">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="6b230-126">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="6b230-127">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="6b230-127">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="6b230-128">Suporte de notificação de evento</span><span class="sxs-lookup"><span data-stu-id="6b230-128">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="6b230-129">Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="6b230-129">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b230-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b230-130">See also</span></span>



[<span data-ttu-id="6b230-131">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="6b230-131">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="6b230-132">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b230-132">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6b230-133">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="6b230-133">MAPI Structures</span></span>](mapi-structures.md)

