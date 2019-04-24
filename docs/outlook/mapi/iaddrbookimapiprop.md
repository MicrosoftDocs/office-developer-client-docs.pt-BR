---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341374"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="b3dd3-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b3dd3-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="b3dd3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3dd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3dd3-105">Dá suporte ao acesso ao catálogo de endereços MAPI e inclui operações como exibir caixas de diálogo comuns; abrir contêineres, usuários de mensagens e listas de distribuição; e executando a resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3dd3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3dd3-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="b3dd3-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b3dd3-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b3dd3-109">Objetos do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="b3dd3-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="b3dd3-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3dd3-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3dd3-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3dd3-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-112">Called by:</span></span>  <br/> |<span data-ttu-id="b3dd3-113">Aplicativos cliente, provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b3dd3-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="b3dd3-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b3dd3-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="b3dd3-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="b3dd3-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b3dd3-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="b3dd3-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="b3dd3-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="b3dd3-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="b3dd3-119">Não gravável</span><span class="sxs-lookup"><span data-stu-id="b3dd3-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b3dd3-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="b3dd3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b3dd3-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b3dd3-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="b3dd3-122">Abre uma entrada do catálogo de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b3dd3-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="b3dd3-124">Compara dois identificadores de entrada que pertencem a um determinado provedor de catálogo de endereços para determinar se eles se referem ao mesmo objeto de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-125">Utilizar</span><span class="sxs-lookup"><span data-stu-id="b3dd3-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="b3dd3-126">Registra um cliente ou provedor de serviços para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-127">Cancelar</span><span class="sxs-lookup"><span data-stu-id="b3dd3-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="b3dd3-128">Cancela um registro de notificação estabelecido previamente para uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b3dd3-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="b3dd3-130">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="b3dd3-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="b3dd3-132">Adiciona um novo destinatário a um contêiner de catálogo de endereços ou à lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-133">Resolvedor</span><span class="sxs-lookup"><span data-stu-id="b3dd3-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="b3dd3-134">Realiza a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-135">Endereço</span><span class="sxs-lookup"><span data-stu-id="b3dd3-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="b3dd3-136">Exibe a caixa de diálogo catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-137">Detalhes</span><span class="sxs-lookup"><span data-stu-id="b3dd3-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="b3dd3-138">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereços específica.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="b3dd3-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="b3dd3-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="b3dd3-140">*Não suportado ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="b3dd3-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="b3dd3-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="b3dd3-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="b3dd3-142">*Não suportado ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="b3dd3-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="b3dd3-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="b3dd3-144">Retorna o identificador de entrada do contêiner designado como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="b3dd3-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="b3dd3-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="b3dd3-146">Designa um determinado contêiner como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="b3dd3-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b3dd3-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="b3dd3-148">Retorna o identificador de entrada para o contêiner do catálogo de endereços inicial.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b3dd3-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="b3dd3-150">Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão inicialmente disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b3dd3-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="b3dd3-152">Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nomes iniciado [](iaddrbook-resolvename.md) pelo método ResolveName.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b3dd3-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="b3dd3-154">Define um novo caminho de pesquisa no perfil usado para o processo de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="b3dd3-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="b3dd3-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="b3dd3-156">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3dd3-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3dd3-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3dd3-157">See also</span></span>



[<span data-ttu-id="b3dd3-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b3dd3-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

