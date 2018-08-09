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
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767165"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="2cfc6-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2cfc6-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="2cfc6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cfc6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cfc6-105">Permite que os clientes, provedores de serviços e MAPI trabalhar com propriedades.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="2cfc6-106">Todos os objetos que oferecem suporte a propriedades implementam esta interface.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cfc6-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-107">Header file:</span></span>  <br/> |<span data-ttu-id="2cfc6-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cfc6-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2cfc6-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2cfc6-110">Nenhum objeto expõe essa interface diretamente.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="2cfc6-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2cfc6-112">Provedores de serviços e MAPI</span><span class="sxs-lookup"><span data-stu-id="2cfc6-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2cfc6-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-113">Called by:</span></span>  <br/> |<span data-ttu-id="2cfc6-114">MAPI, provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="2cfc6-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="2cfc6-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2cfc6-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2cfc6-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="2cfc6-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2cfc6-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="2cfc6-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="2cfc6-119">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="2cfc6-120">Classe abstrata, nunca implementada</span><span class="sxs-lookup"><span data-stu-id="2cfc6-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2cfc6-121">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="2cfc6-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2cfc6-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2cfc6-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="2cfc6-123">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2cfc6-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="2cfc6-125">Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="2cfc6-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="2cfc6-127">Recupera o valor da propriedade de uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-128">GetPropList</span><span class="sxs-lookup"><span data-stu-id="2cfc6-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="2cfc6-129">Retorna as marcas de propriedade para todas as propriedades.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="2cfc6-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="2cfc6-131">Retorna um ponteiro para uma interface que pode ser usada para acessar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="2cfc6-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="2cfc6-133">Atualiza uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="2cfc6-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="2cfc6-135">Exclui uma ou mais propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="2cfc6-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="2cfc6-137">Copia ou move todas as propriedades, exceto especificamente propriedades excluídas.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="2cfc6-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="2cfc6-139">Cópias ou movimentações de propriedades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="2cfc6-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="2cfc6-141">Fornece os nomes de propriedades que correspondem a um ou mais identificadores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="2cfc6-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="2cfc6-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="2cfc6-143">Fornece os identificadores de propriedade que correspondem a um ou mais nomes de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2cfc6-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cfc6-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cfc6-144">Remarks</span></span>

 <span data-ttu-id="2cfc6-145">**IMAPIProp** é a interface de base para as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="2cfc6-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="2cfc6-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="2cfc6-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="2cfc6-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="2cfc6-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="2cfc6-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2cfc6-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="2cfc6-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="2cfc6-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="2cfc6-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="2cfc6-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="2cfc6-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="2cfc6-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="2cfc6-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="2cfc6-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="2cfc6-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="2cfc6-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="2cfc6-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="2cfc6-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="2cfc6-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cfc6-155">See also</span></span>



[<span data-ttu-id="2cfc6-156">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2cfc6-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

