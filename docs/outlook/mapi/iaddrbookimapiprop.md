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
ms.openlocfilehash: 0e39f2603a1eef45c456b7fb58744b79c6b75f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766876"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="664d5-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="664d5-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="664d5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="664d5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="664d5-105">Oferece suporte ao acesso ao catálogo de endereços MAPI e inclui operações como exibir caixas de diálogo comuns; contêineres de abertura, mensagens de usuários e listas de distribuição; e executar a resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="664d5-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="664d5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="664d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="664d5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="664d5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="664d5-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="664d5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="664d5-109">Objetos de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="664d5-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="664d5-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="664d5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="664d5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="664d5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="664d5-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="664d5-112">Called by:</span></span>  <br/> |<span data-ttu-id="664d5-113">Aplicativos clientes, provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="664d5-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="664d5-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="664d5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="664d5-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="664d5-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="664d5-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="664d5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="664d5-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="664d5-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="664d5-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="664d5-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="664d5-119">Não gravável</span><span class="sxs-lookup"><span data-stu-id="664d5-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="664d5-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="664d5-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="664d5-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="664d5-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="664d5-122">Abre uma entrada do catálogo de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.</span><span class="sxs-lookup"><span data-stu-id="664d5-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="664d5-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="664d5-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="664d5-124">Compara dois identificadores de entrada que pertencem a um provedor de catálogo de endereço específico para determinar se eles se referem ao mesmo objeto de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="664d5-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="664d5-125">Aviso</span><span class="sxs-lookup"><span data-stu-id="664d5-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="664d5-126">Registra um provedor de serviço ou cliente para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="664d5-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="664d5-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="664d5-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="664d5-128">Cancela um registro de notificação que tenha estabelecido para uma entrada do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="664d5-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="664d5-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="664d5-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="664d5-130">Cria um identificador de entrada para um endereço one-off.</span><span class="sxs-lookup"><span data-stu-id="664d5-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="664d5-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="664d5-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="664d5-132">Adiciona um novo destinatário para um contêiner de catálogo de endereços ou a lista de destinatários de uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="664d5-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="664d5-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="664d5-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="664d5-134">Executa a resolução de nomes, atribuindo identificadores de entrada para destinatários em uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="664d5-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="664d5-135">Endereço</span><span class="sxs-lookup"><span data-stu-id="664d5-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="664d5-136">Exibe a caixa de diálogo do catálogo de endereços do Outlook.</span><span class="sxs-lookup"><span data-stu-id="664d5-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="664d5-137">Detalhes</span><span class="sxs-lookup"><span data-stu-id="664d5-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="664d5-138">Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="664d5-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="664d5-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="664d5-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="664d5-140">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="664d5-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="664d5-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="664d5-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="664d5-142">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="664d5-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="664d5-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="664d5-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="664d5-144">Retorna o identificador de entrada do contêiner que é designado como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="664d5-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="664d5-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="664d5-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="664d5-146">Designa um contêiner específico como o catálogo de endereços pessoal (PAB).</span><span class="sxs-lookup"><span data-stu-id="664d5-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="664d5-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="664d5-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="664d5-148">Retorna o identificador de entrada para o contêiner de catálogo de endereços inicial.</span><span class="sxs-lookup"><span data-stu-id="664d5-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="664d5-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="664d5-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="664d5-150">Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão que inicialmente é disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="664d5-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="664d5-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="664d5-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="664d5-152">Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nome iniciado pelo método [ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="664d5-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="664d5-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="664d5-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="664d5-154">Define um novo caminho de pesquisa no perfil que é usado para o processo de resolução de nome.</span><span class="sxs-lookup"><span data-stu-id="664d5-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="664d5-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="664d5-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="664d5-156">Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="664d5-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="664d5-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="664d5-157">See also</span></span>



[<span data-ttu-id="664d5-158">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="664d5-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

