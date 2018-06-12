---
title: Suporte a formulários e modos de exibição em repositórios de mensagem de somente leitura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1ef9b85fd8dad980f92f5e06a4b54daf146fbcec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770536"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="7b499-103">Suporte a formulários e modos de exibição em repositórios de mensagem de somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b499-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="7b499-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b499-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b499-105">Se seu provedor de armazenamento de mensagens permite que a permissão somente leitura para o mecanismo de armazenamento subjacente, os aplicativos cliente e o Gerenciador de formulário MAPI poderão realizar certas tarefas.</span><span class="sxs-lookup"><span data-stu-id="7b499-105">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things.</span></span> <span data-ttu-id="7b499-106">Especificamente, os clientes não poderão adicionar ou modificar modos de exibição personalizados e o Gerenciador de formulário MAPI poderão instalar formulários nas tabelas de pastas do repositório de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="7b499-106">Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="7b499-107">Para muitos repositórios de mensagem de somente leitura, que pode não ser um problema.</span><span class="sxs-lookup"><span data-stu-id="7b499-107">For many read-only message stores, that may not be a problem.</span></span> <span data-ttu-id="7b499-108">Se for esse o caso, o provedor de armazenamento de mensagem não precisa oferecer suporte a tabelas de conteúdo associado nisso.</span><span class="sxs-lookup"><span data-stu-id="7b499-108">If that is the case, the message store provider does not need to support associated contents tables at all.</span></span> <span data-ttu-id="7b499-109">No entanto, se seu provedor de armazenamento de mensagem deve ser somente leitura e ele também deve oferecer suporte a um conjunto predefinido de formulários ou modos de exibição, será necessário dar suporte a tabelas de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="7b499-109">However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="7b499-110">A estratégia mais comuns para fazer isso, porque os clientes e o Gerenciador de formulário MAPI não é possível instalar os modos de exibição ou formulários na mensagem armazenam sozinhos, é para o provedor de armazenamento de mensagem codificá--los para o repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7b499-110">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store.</span></span> <span data-ttu-id="7b499-111">Isso significa que a tabela de conteúdo associados ou tabelas que contêm os modos de exibição ou formulários continuará a existir no repositório de mensagem quando ele é criado, antes de todos os clientes ou MAPI Gerenciador de formulário nunca acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="7b499-111">This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it.</span></span> <span data-ttu-id="7b499-112">Em seguida, quando um cliente solicitar uma tabela de conteúdo associado ao fazer exibições personalizadas a partir de um formulário ou o Gerenciador de formulário MAPI solicita uma tabela de conteúdo associado à inicialização de um formulário, o provedor de armazenamento de mensagens pode fornecer uma.</span><span class="sxs-lookup"><span data-stu-id="7b499-112">Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="7b499-113">Esse requisito que as tabelas de conteúdo associado deve ser criadas e preenchidas quando o armazenamento de mensagens em si é criado indica que o seu provedor de armazenamento de mensagem precisará obter informações sobre o formato das mensagens especiais que clientes e o formulário MAPI Gerenciador de usar para armazenar os modos de exibição e formulários.</span><span class="sxs-lookup"><span data-stu-id="7b499-113">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms.</span></span> <span data-ttu-id="7b499-114">Cite empregar esses formatos dependerá o cliente e o Gerenciador de formulário MAPI que está sendo usado, portanto, uma descrição que eles não pode ser fornecida aqui.</span><span class="sxs-lookup"><span data-stu-id="7b499-114">What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b499-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b499-115">See also</span></span>



[<span data-ttu-id="7b499-116">Repositórios de mensagem de somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b499-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

