---
title: Repositórios de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766363"
---
# <a name="default-message-stores"></a><span data-ttu-id="e122f-103">Repositórios de mensagens padrão</span><span class="sxs-lookup"><span data-stu-id="e122f-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="e122f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e122f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e122f-105">Um armazenamento de mensagens padrão é aquela que aplicativos cliente podem usar para tarefas de mensagens de finalidade geral.</span><span class="sxs-lookup"><span data-stu-id="e122f-105">A default message store is one that client applications can use for general purpose messaging tasks.</span></span> <span data-ttu-id="e122f-106">Há um número de recursos opcionais para provedores de armazenamento de mensagem que se tornam necessários se o provedor de armazenamento de mensagem deve ser usado como o armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="e122f-106">There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store.</span></span> <span data-ttu-id="e122f-107">Eles são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e122f-107">They are as follows:</span></span>
  
- <span data-ttu-id="e122f-108">Implementando pastas especiais: as pastas de caixa de entrada, caixa de saída e os resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e122f-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="e122f-109">Fornecimento de relatórios de leitura e nonread.</span><span class="sxs-lookup"><span data-stu-id="e122f-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="e122f-110">Permitindo que envios de mensagem de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="e122f-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="e122f-111">Permitindo a criação de mensagens com classes de mensagens arbitrário.</span><span class="sxs-lookup"><span data-stu-id="e122f-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="e122f-112">Dando suporte a propriedades nomeadas e de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="e122f-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="e122f-113">Suporte ao método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) , mesmo se o provedor de armazenamento de mensagem está firmemente combinado com um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e122f-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="e122f-114">Tabelas de conteúdo associado de suporte.</span><span class="sxs-lookup"><span data-stu-id="e122f-114">Supporting associated contents tables.</span></span> <span data-ttu-id="e122f-115">Para obter mais informações, consulte [As tabelas de conteúdo](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e122f-115">For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="e122f-116">Dando suporte a notificação do spooler MAPI quando há mensagens na fila de mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="e122f-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e122f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e122f-117">See also</span></span>



[<span data-ttu-id="e122f-118">Desenvolver um provedor do repositório de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="e122f-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

