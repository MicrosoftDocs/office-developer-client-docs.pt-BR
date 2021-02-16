---
title: Suporte a formulários e exibições em Read-Only de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432426"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="0126d-103">Suporte a formulários e exibições em Read-Only de mensagens</span><span class="sxs-lookup"><span data-stu-id="0126d-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="0126d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0126d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0126d-105">Se seu provedor de armazenamento de mensagens permitir permissão somente leitura para o mecanismo de armazenamento subjacente, os aplicativos cliente e o gerenciador de formulário MAPI não poderão fazer determinadas coisas.</span><span class="sxs-lookup"><span data-stu-id="0126d-105">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things.</span></span> <span data-ttu-id="0126d-106">Especificamente, os clientes não poderão adicionar ou modificar exibições personalizadas, e o gerenciador de formulários MAPI não poderá instalar formulários nas tabelas de conteúdo associadas das pastas do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0126d-106">Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="0126d-107">Para muitos armazenamentos de mensagens somente leitura, isso pode não ser um problema.</span><span class="sxs-lookup"><span data-stu-id="0126d-107">For many read-only message stores, that may not be a problem.</span></span> <span data-ttu-id="0126d-108">Se esse for o caso, o provedor de armazenamento de mensagens não precisa dar suporte a tabelas de conteúdo associadas.</span><span class="sxs-lookup"><span data-stu-id="0126d-108">If that is the case, the message store provider does not need to support associated contents tables at all.</span></span> <span data-ttu-id="0126d-109">No entanto, se seu provedor de armazenamento de mensagens deve ser somente leitura e também deve suportar um conjunto predefinido de exibições ou formulários, ele precisará dar suporte a tabelas de conteúdo associadas.</span><span class="sxs-lookup"><span data-stu-id="0126d-109">However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="0126d-110">A estratégia mais comum para fazer isso, porque os clientes e o gerenciador de formulários MAPI não podem instalar os próprios formulários ou exibições no armazenamento de mensagens, é que o provedor de armazenamento de mensagens os codifica no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0126d-110">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store.</span></span> <span data-ttu-id="0126d-111">Isso significa que a tabela ou tabelas de conteúdo associadas que contêm os formulários ou exibições existirão no armazenamento de mensagens quando ele for criado, antes de qualquer cliente ou o gerenciador de formulários MAPI acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="0126d-111">This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it.</span></span> <span data-ttu-id="0126d-112">Em seguida, quando um cliente solicita uma tabela de conteúdo associada para obter exibições personalizadas de um formulário ou o gerenciador de formulário MAPI solicita uma tabela de conteúdo associada para iniciar um formulário, o provedor de armazenamento de mensagens pode fornecer um.</span><span class="sxs-lookup"><span data-stu-id="0126d-112">Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="0126d-113">Esse requisito de que as tabelas de conteúdo associadas sejam criadas e preenchidas quando o próprio armazenamento de mensagens for criado implica em que seu provedor de armazenamento de mensagens precisará obter informações sobre o formato das mensagens especiais que os clientes e o gerenciador de formulários MAPI usam para armazenar exibições e formulários.</span><span class="sxs-lookup"><span data-stu-id="0126d-113">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms.</span></span> <span data-ttu-id="0126d-114">O uso desses formatos dependerá do cliente e do gerenciador de formulário MAPI, portanto, uma descrição deles não pode ser fornecida aqui.</span><span class="sxs-lookup"><span data-stu-id="0126d-114">What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0126d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0126d-115">See also</span></span>



[<span data-ttu-id="0126d-116">Armazenamentos de Mensagens Somente Leitura</span><span class="sxs-lookup"><span data-stu-id="0126d-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

