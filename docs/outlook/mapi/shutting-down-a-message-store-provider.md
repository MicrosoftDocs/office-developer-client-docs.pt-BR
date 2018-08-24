---
title: Desligar um provedor do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1c7ae4ab6de20d69581a98323c14a2c15f436cad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572820"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="54d00-103">Desligar um provedor do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="54d00-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="54d00-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54d00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54d00-105">Se seu provedor for um provedor de armazenamento de mensagem, ele pode ser desligado em uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="54d00-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="54d00-106">Quando um cliente ou o MAPI spooler chama [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="54d00-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="54d00-107">Encerrando um provedor de armazenamento de mensagem com **StoreLogoff** faz com que o desligamento ocorra uma maneira ordenada e controlada.</span><span class="sxs-lookup"><span data-stu-id="54d00-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="54d00-108">Quando um cliente chama [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="54d00-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="54d00-109">A implementação dos **IMsgStore::StoreLogoff** deve começar chamando [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar MAPI que está sendo desligado, indicando que qualquer provedor de transporte relacionados deve ser desconectado.</span><span class="sxs-lookup"><span data-stu-id="54d00-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="54d00-110">Quando **IMsgStore::StoreLogoff** retorna, seu chamador chama o método de [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do seu armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="54d00-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="54d00-111">Implemente esse método **versão** chamando-se o suporte ao método do objeto **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="54d00-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="54d00-112">MAPI executa as seguintes tarefas em sua implementação do **IUnknown:: Release** para repositórios de mensagem:</span><span class="sxs-lookup"><span data-stu-id="54d00-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="54d00-113">Remove todas as estruturas [MAPIUID](mapiuid.md) registradas pelo provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="54d00-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="54d00-114">Remove a linha do provedor de repositório a mensagem da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="54d00-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="54d00-115">Chama [IMSLogon::Logoff](imslogon-logoff.md) para liberar todos os objetos abertos, subobjetos e objetos de status.</span><span class="sxs-lookup"><span data-stu-id="54d00-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="54d00-116">Chama [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto de logon do provedor de repositório a mensagem.</span><span class="sxs-lookup"><span data-stu-id="54d00-116">Calls [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="54d00-117">Alguns clientes podem omitir a chamada para **IMsgStore::StoreLogoff**, iniciando o desligamento do seu provedor de armazenamento de mensagem com a chamada ao método de **IUnknown:: Release** do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="54d00-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="54d00-118">Um desligamento seguintes circunstâncias sem a chamada para **StoreLogoff** é menos ordenado e controlada.</span><span class="sxs-lookup"><span data-stu-id="54d00-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="54d00-119">Escreva o método de **lançamento** do armazenamento de suas mensagens para lidar com essa possibilidade e ficar atento se ou não uma chamada para **IMAPISupport::StoreLogoffTransports** ocorreu.</span><span class="sxs-lookup"><span data-stu-id="54d00-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="54d00-120">**StoreLogoffTransports** deve ser chamada uma vez durante o processo de desligamento.</span><span class="sxs-lookup"><span data-stu-id="54d00-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="54d00-121">Se você detectar no seu método de **versão** que **StoreLogoffTransports** ainda não foi chamado, chamá-la com o sinalizador LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="54d00-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="54d00-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="54d00-122">See also</span></span>



[<span data-ttu-id="54d00-123">Desligar a um provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="54d00-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

