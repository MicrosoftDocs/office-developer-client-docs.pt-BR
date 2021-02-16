---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413378"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="7b8fe-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b8fe-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="7b8fe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b8fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b8fe-105">Gerencia objetos associados a uma sessão de logon MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b8fe-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b8fe-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="7b8fe-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="7b8fe-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7b8fe-109">Objetos Session</span><span class="sxs-lookup"><span data-stu-id="7b8fe-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="7b8fe-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b8fe-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8fe-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b8fe-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-112">Called by:</span></span>  <br/> |<span data-ttu-id="7b8fe-113">Aplicativos cliente e MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8fe-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="7b8fe-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7b8fe-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="7b8fe-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="7b8fe-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="7b8fe-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7b8fe-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="7b8fe-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7b8fe-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="7b8fe-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7b8fe-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="7b8fe-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="7b8fe-120">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro de sessão anterior.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="7b8fe-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="7b8fe-122">Fornece acesso à tabela do armazenamento de mensagens que contém informações sobre todos os armazenamentos de mensagens no perfil de sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="7b8fe-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="7b8fe-124">Abre um repositório de mensagens e retorna um ponteiro [IMsgStore](imsgstoreimapiprop.md) para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="7b8fe-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="7b8fe-126">Abre o livro de endereços integrado MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7b8fe-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="7b8fe-128">Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="7b8fe-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="7b8fe-130">Fornece acesso à tabela de status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="7b8fe-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="7b8fe-132">Abre um objeto e retorna um ponteiro de interface para mais acesso.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="7b8fe-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="7b8fe-134">Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-135">Advise</span><span class="sxs-lookup"><span data-stu-id="7b8fe-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="7b8fe-136">Registra para receber notificação de eventos especificados que afetam a sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="7b8fe-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="7b8fe-138">Cancela o envio de notificações configuradas anteriormente com uma chamada para o **método Advise.**</span><span class="sxs-lookup"><span data-stu-id="7b8fe-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="7b8fe-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="7b8fe-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="7b8fe-140">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="7b8fe-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="7b8fe-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="7b8fe-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="7b8fe-142">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="7b8fe-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="7b8fe-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="7b8fe-144">Depreciado.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-144">Deprecated.</span></span> <span data-ttu-id="7b8fe-145">Retorna os tipos de endereço que podem ser manipulados por todos os provedores de transporte na sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="7b8fe-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="7b8fe-147">Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-148">Fazer logoff</span><span class="sxs-lookup"><span data-stu-id="7b8fe-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="7b8fe-149">Encerra uma sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="7b8fe-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="7b8fe-151">Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="7b8fe-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="7b8fe-153">Retorna um [ponteiro IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações nos serviços de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="7b8fe-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="7b8fe-155">Exibe um formulário.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="7b8fe-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="7b8fe-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="7b8fe-157">Cria um token numérico que o **método ShowForm** usa para acessar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7b8fe-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b8fe-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b8fe-158">See also</span></span>



[<span data-ttu-id="7b8fe-159">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7b8fe-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

