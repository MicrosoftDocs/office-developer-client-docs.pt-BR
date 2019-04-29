---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429625"
---
# <a name="notifkey"></a><span data-ttu-id="1ed68-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="1ed68-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="1ed68-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ed68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ed68-105">Identifica exclusivamente uma conexão entre um coletor de aviso, uma fonte de aviso e MAPI.</span><span class="sxs-lookup"><span data-stu-id="1ed68-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ed68-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ed68-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ed68-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="1ed68-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="1ed68-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ed68-108">Members</span></span>

 <span data-ttu-id="1ed68-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="1ed68-109">**cb**</span></span>
  
> <span data-ttu-id="1ed68-110">Contagem de bytes no membro **AB** .</span><span class="sxs-lookup"><span data-stu-id="1ed68-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="1ed68-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="1ed68-111">**ab**</span></span>
  
> <span data-ttu-id="1ed68-112">Matriz de bytes que descreve a chave de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ed68-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ed68-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ed68-113">Remarks</span></span>

<span data-ttu-id="1ed68-114">Os métodos [Subscribe](imapisupport-subscribe.md) e [Notify](imapisupport-notify.md) do [IMAPISupport](imapisupportiunknown.md) usam a estrutura **NOTIFKEY** para gerar notificações para o coletor de aviso apropriado sobre a fonte de aviso apropriada.</span><span class="sxs-lookup"><span data-stu-id="1ed68-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="1ed68-115">Os provedores de serviços geram chaves de notificação quando o método **Advise** é chamado e querem chamar **inscrever-se** para lidar com o registro de notificação e o envio subsequente de notificações.</span><span class="sxs-lookup"><span data-stu-id="1ed68-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="1ed68-116">Uma chave de notificação pode ser o identificador de entrada da fonte de aviso ou pode ser qualquer outro item de identificação, como uma constante.</span><span class="sxs-lookup"><span data-stu-id="1ed68-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="1ed68-117">Por exemplo, um provedor de repositório de mensagens pode usar o caminho de uma pasta como sua chave de notificação.</span><span class="sxs-lookup"><span data-stu-id="1ed68-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="1ed68-118">A chave de notificação deve funcionar em vários processos.</span><span class="sxs-lookup"><span data-stu-id="1ed68-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="1ed68-119">Os requisitos de escopo para uma chave de notificação se assemelham a um identificador de entrada de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="1ed68-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="1ed68-120">No enTanto, ao contrário de um identificador de entrada, uma chave de notificação deve ser comparável ao binário.</span><span class="sxs-lookup"><span data-stu-id="1ed68-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="1ed68-121">Normalmente, uma chave de notificação inclui um valor de **GUID** definido pelo provedor de serviços seguido por outras informações específicas do provedor exclusivas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="1ed68-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="1ed68-122">Para obter uma discussão sobre o uso da estrutura **NOTIFKEY** para gerenciar as conexões entre os coletores de aviso e os objetos que geram notificações, consulte [support Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="1ed68-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ed68-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ed68-123">See also</span></span>



[<span data-ttu-id="1ed68-124">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ed68-124">MAPI Structures</span></span>](mapi-structures.md)

