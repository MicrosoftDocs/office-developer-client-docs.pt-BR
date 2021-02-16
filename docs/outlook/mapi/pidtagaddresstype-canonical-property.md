---
title: Propriedade canônica PidTagAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressType
api_type:
- HeaderDef
ms.assetid: 986719d2-8837-46b4-8d04-c24508f5e19a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6051d3403cede21fa4aebdb6ca561dd3efb46771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360079"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="96a37-103">Propriedade canônica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="96a37-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="96a37-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96a37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96a37-105">Contém o tipo de endereço de email do usuário de mensagens, como SMTP.</span><span class="sxs-lookup"><span data-stu-id="96a37-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96a37-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="96a37-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="96a37-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="96a37-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="96a37-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="96a37-108">Identifier:</span></span>  <br/> |<span data-ttu-id="96a37-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="96a37-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="96a37-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="96a37-110">Data type:</span></span>  <br/> |<span data-ttu-id="96a37-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="96a37-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="96a37-112">Área:</span><span class="sxs-lookup"><span data-stu-id="96a37-112">Area:</span></span>  <br/> |<span data-ttu-id="96a37-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="96a37-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96a37-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="96a37-114">Remarks</span></span>

<span data-ttu-id="96a37-115">Essas propriedades são exemplos das propriedades de endereço base comuns a todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="96a37-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="96a37-116">Ele especifica qual sistema de mensagens MAPI usa para lidar com uma determinada mensagem.</span><span class="sxs-lookup"><span data-stu-id="96a37-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="96a37-117">Essa propriedade também determina o formato da cadeia de caracteres de endereço no **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="96a37-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="96a37-118">A cadeia de caracteres que ele fornece pode conter somente os caracteres alfabéticos em maiúsculas de A a Z e os números de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="96a37-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="96a37-119">Exemplos válidos para a cadeia de caracteres incluem:</span><span class="sxs-lookup"><span data-stu-id="96a37-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="96a37-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="96a37-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="96a37-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="96a37-121">Protocol specifications</span></span>

<span data-ttu-id="96a37-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-123">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="96a37-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="96a37-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-124">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-125">Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="96a37-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="96a37-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-126">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-127">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="96a37-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="96a37-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-128">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-129">Lida com as comunicações de um cliente com um servidor NSPI (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="96a37-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="96a37-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-130">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-131">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="96a37-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="96a37-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-132">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-133">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="96a37-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="96a37-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-134">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-135">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="96a37-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="96a37-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-136">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-137">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="96a37-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="96a37-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-138">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-139">Especifica operações permitidas para os objetos principais do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="96a37-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="96a37-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-140">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-141">Especifica as propriedades e operações que são permitidas para modelos de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="96a37-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="96a37-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-143">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="96a37-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="96a37-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-144">[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-145">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="96a37-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="96a37-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="96a37-146">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="96a37-147">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="96a37-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="96a37-148">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="96a37-148">Header files</span></span>

<span data-ttu-id="96a37-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="96a37-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="96a37-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="96a37-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="96a37-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="96a37-151">Mapitags.h</span></span>
  
> <span data-ttu-id="96a37-152">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="96a37-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="96a37-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="96a37-153">See also</span></span>



[<span data-ttu-id="96a37-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="96a37-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="96a37-155">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="96a37-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="96a37-156">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="96a37-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="96a37-157">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="96a37-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="96a37-158">Tipos de endereço MAPI</span><span class="sxs-lookup"><span data-stu-id="96a37-158">MAPI Address Types</span></span>](mapi-address-types.md)

