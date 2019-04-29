---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa as configurações de transporte que o Outlook usa para determinar as tarefas de sincronização necessárias e para desabilitar os elementos da interface do usuário que a conta não suporta.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404523"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="f310a-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f310a-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="f310a-104">Representa as configurações de transporte que o Outlook usa para determinar as tarefas de sincronização necessárias e para desabilitar os elementos da interface do usuário que a conta não suporta.</span><span class="sxs-lookup"><span data-stu-id="f310a-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f310a-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f310a-105">Quick info</span></span>

<span data-ttu-id="f310a-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="f310a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f310a-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f310a-107">Identifier:</span></span>  <br/> |<span data-ttu-id="f310a-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="f310a-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="f310a-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f310a-109">Property type:</span></span>  <br/> |<span data-ttu-id="f310a-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f310a-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f310a-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f310a-111">Property tag:</span></span>  <br/> |<span data-ttu-id="f310a-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="f310a-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="f310a-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="f310a-113">Access:</span></span>  <br/> |<span data-ttu-id="f310a-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="f310a-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f310a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f310a-115">Remarks</span></span>

<span data-ttu-id="f310a-116">Obter ou definir essa propriedade usando [IOlkAccount:: GetProp](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f310a-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="f310a-117">Retorna **MAPIACCT_SEND_ONLY** se a conta só puder enviar mensagens, mas não puder receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="f310a-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="f310a-118">Nesse caso, o Outlook desabilita a IU que não se aplica a esse tipo de conta (por exemplo, a interface do usuário para **Enviar/receber**).</span><span class="sxs-lookup"><span data-stu-id="f310a-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f310a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f310a-119">See also</span></span>

- [<span data-ttu-id="f310a-120">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="f310a-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="f310a-121">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="f310a-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

