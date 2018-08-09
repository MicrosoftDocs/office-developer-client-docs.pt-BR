---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa as configurações de transporte que o Outlook usa para determinar as tarefas necessárias de sincronização e desabilitar os elementos de interface (UI) do usuário que a conta não oferece suporte.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766061"
---
# <a name="propmapitransportflags"></a><span data-ttu-id="1643c-103">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1643c-103">PROP_MAPI_TRANSPORT_FLAGS</span></span>

<span data-ttu-id="1643c-104">Representa as configurações de transporte que o Outlook usa para determinar as tarefas necessárias de sincronização e desabilitar os elementos de interface (UI) do usuário que a conta não oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="1643c-104">Represents transport settings that Outlook uses to determine the necessary synchronization tasks and to disable the user interface (UI) elements that the account does not support.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1643c-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1643c-105">Quick info</span></span>

<span data-ttu-id="1643c-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="1643c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1643c-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1643c-107">Identifier:</span></span>  <br/> |<span data-ttu-id="1643c-108">0x2010</span><span class="sxs-lookup"><span data-stu-id="1643c-108">0x2010</span></span>  <br/> |
|<span data-ttu-id="1643c-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="1643c-109">Property type:</span></span>  <br/> |<span data-ttu-id="1643c-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1643c-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1643c-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="1643c-111">Property tag:</span></span>  <br/> |<span data-ttu-id="1643c-112">0x20100102</span><span class="sxs-lookup"><span data-stu-id="1643c-112">0x20100102</span></span>  <br/> |
|<span data-ttu-id="1643c-113">Access:</span><span class="sxs-lookup"><span data-stu-id="1643c-113">Access:</span></span>  <br/> |<span data-ttu-id="1643c-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1643c-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1643c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1643c-115">Remarks</span></span>

<span data-ttu-id="1643c-116">Obter ou definir essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1643c-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="1643c-117">Retorna **MAPIACCT_SEND_ONLY** se a conta só pode enviar mensagens, mas não pode receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="1643c-117">Returns **MAPIACCT_SEND_ONLY** if the account can only send messages but cannot receive messages.</span></span> <span data-ttu-id="1643c-118">Nesse caso, Outlook desabilita a interface do usuário que não se aplica a esse tipo de contas (por exemplo, a interface do usuário para **Envio/recebimento**).</span><span class="sxs-lookup"><span data-stu-id="1643c-118">In this case, Outlook disables UI that does not apply to this type of accounts (for example, the UI for **Send/Receive**).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1643c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="1643c-119">See also</span></span>

- [<span data-ttu-id="1643c-120">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="1643c-120">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="1643c-121">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="1643c-121">Constants (Account management API)</span></span>](constants-account-management-api.md)

