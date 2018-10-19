---
title: Repositórios de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576908"
---
# <a name="default-message-stores"></a><span data-ttu-id="3a4d0-103">Repositórios de mensagens padrão</span><span class="sxs-lookup"><span data-stu-id="3a4d0-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="3a4d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a4d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a4d0-105">Um repositório de mensagens padrão é aquele que os aplicativos de clientes podem usar para tarefas de mensagens de finalidade geral.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-105">A default message store is one that client applications can use for general purpose messaging tasks.</span></span> <span data-ttu-id="3a4d0-106">Há vários recursos opcionais de provedores de repositórios de mensagens que se tornam necessários se o provedor do repositório de mensagens precisar ser usado como repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-106">There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store.</span></span> <span data-ttu-id="3a4d0-107">São eles:</span><span class="sxs-lookup"><span data-stu-id="3a4d0-107">They are as follows:</span></span>
  
- <span data-ttu-id="3a4d0-108">Implementar as pastas especiais: as pastas de caixa de entrada e saída e de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="3a4d0-109">Fornecer relatórios de leitura e não leitura.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="3a4d0-110">Permitir envios de mensagens de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="3a4d0-111">Permitir a criação de mensagens com classes de mensagem arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="3a4d0-112">Suportar propriedades nomeadas e de múltiplos valores.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="3a4d0-113">Suportar o método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), mesmo que o provedor do repositório de mensagens esteja fortemente acoplado a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="3a4d0-114">Suportar tabelas de conteúdo associados.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-114">Supporting associated contents tables.</span></span> <span data-ttu-id="3a4d0-115">Para mais informações, confira [Tabelas de Conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3a4d0-115">For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="3a4d0-116">Suporte à notificação do spooler MAPI quando há mensagens na fila de mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="3a4d0-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3a4d0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a4d0-117">See also</span></span>



[<span data-ttu-id="3a4d0-118">Desenvolver um provedor de repositórios de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="3a4d0-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

