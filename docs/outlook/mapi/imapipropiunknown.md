---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407659"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="5a381-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a381-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="5a381-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a381-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a381-105">Permite que clientes, provedores de serviços e MAPI trabalhem com propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a381-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="5a381-106">Todos os objetos que dão suporte a Propriedades implementam essa interface.</span><span class="sxs-lookup"><span data-stu-id="5a381-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a381-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5a381-107">Header file:</span></span>  <br/> |<span data-ttu-id="5a381-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5a381-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a381-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="5a381-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="5a381-110">Nenhum objeto expõe esta interface diretamente.</span><span class="sxs-lookup"><span data-stu-id="5a381-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="5a381-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5a381-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a381-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="5a381-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="5a381-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5a381-113">Called by:</span></span>  <br/> |<span data-ttu-id="5a381-114">Aplicativos cliente, provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="5a381-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="5a381-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="5a381-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5a381-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5a381-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="5a381-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="5a381-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="5a381-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="5a381-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="5a381-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="5a381-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="5a381-120">Classe abstrata, nunca implementado</span><span class="sxs-lookup"><span data-stu-id="5a381-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5a381-121">Vtable order</span><span class="sxs-lookup"><span data-stu-id="5a381-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5a381-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5a381-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="5a381-123">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="5a381-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="5a381-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5a381-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="5a381-125">Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="5a381-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="5a381-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="5a381-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="5a381-127">Recupera o valor da propriedade de uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="5a381-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="5a381-128">GetProplist</span><span class="sxs-lookup"><span data-stu-id="5a381-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="5a381-129">Retorna as marcas de propriedade de todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a381-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="5a381-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5a381-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="5a381-131">Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a381-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="5a381-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="5a381-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="5a381-133">Atualiza uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a381-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="5a381-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="5a381-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="5a381-135">Exclui uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="5a381-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="5a381-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="5a381-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="5a381-137">Copia ou move todas as propriedades, exceto as propriedades especificamente excluídas.</span><span class="sxs-lookup"><span data-stu-id="5a381-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="5a381-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="5a381-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="5a381-139">Copia ou move as propriedades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="5a381-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="5a381-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="5a381-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="5a381-141">Fornece os nomes de propriedade que correspondem a um ou mais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a381-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="5a381-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="5a381-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="5a381-143">Fornece os identificadores de propriedade que correspondem a um ou mais nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="5a381-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a381-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a381-144">Remarks</span></span>

 <span data-ttu-id="5a381-145">**IMAPIProp** é a interface base para as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="5a381-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="5a381-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="5a381-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="5a381-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="5a381-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="5a381-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5a381-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="5a381-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="5a381-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="5a381-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="5a381-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="5a381-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="5a381-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="5a381-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="5a381-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="5a381-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="5a381-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="5a381-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="5a381-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="5a381-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a381-155">See also</span></span>



[<span data-ttu-id="5a381-156">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5a381-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

