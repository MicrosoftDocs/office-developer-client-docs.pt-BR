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
ms.openlocfilehash: 5398519dc841aa72f2c2655aac6c9f7acba7f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768938"
---
# <a name="pidtagaddresstype-canonical-property"></a><span data-ttu-id="20e78-103">Propriedade canônica PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="20e78-103">PidTagAddressType Canonical Property</span></span>

<span data-ttu-id="20e78-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="20e78-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="20e78-105">Contém o tipo de endereço de email de mensagens do usuário, como o SMTP.</span><span class="sxs-lookup"><span data-stu-id="20e78-105">Contains the messaging user's email address type, such as SMTP.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20e78-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="20e78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20e78-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="20e78-107">PR_ADDRTYPE, PR_ADDRTYPE_A, PR_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="20e78-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="20e78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20e78-109">0x3002</span><span class="sxs-lookup"><span data-stu-id="20e78-109">0x3002</span></span>  <br/> |
|<span data-ttu-id="20e78-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="20e78-110">Data type:</span></span>  <br/> |<span data-ttu-id="20e78-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="20e78-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="20e78-112">Área:</span><span class="sxs-lookup"><span data-stu-id="20e78-112">Area:</span></span>  <br/> |<span data-ttu-id="20e78-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="20e78-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20e78-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="20e78-114">Remarks</span></span>

<span data-ttu-id="20e78-115">Essas propriedades são exemplos das propriedades endereço base comuns a todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="20e78-115">These properties are examples of the base address properties common to all messaging users.</span></span> <span data-ttu-id="20e78-116">Especifica qual sistema de mensagens MAPI usa para lidar com uma determinada mensagem.</span><span class="sxs-lookup"><span data-stu-id="20e78-116">It specifies which messaging system MAPI uses to handle a given message.</span></span>
  
<span data-ttu-id="20e78-117">Essa propriedade também determina o formato da cadeia de caracteres de endereço em **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="20e78-117">This property also determines the format of the address string in the **PR_EMAIL_ADRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)).</span></span> <span data-ttu-id="20e78-118">Ele fornece a cadeia de caracteres pode conter apenas os caracteres alfabéticos maiusculos de À Z e os números de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="20e78-118">The string it provides can contain only the uppercase alphabetic characters from A through Z and the numbers from 0 through 9.</span></span>
  
<span data-ttu-id="20e78-119">Exemplos válidos da cadeia de caracteres incluem:</span><span class="sxs-lookup"><span data-stu-id="20e78-119">Valid examples for the string include:</span></span> 
  
```cpp
FAX
MHS
PROFS
SMTP
X400

```

## <a name="related-resources"></a><span data-ttu-id="20e78-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20e78-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20e78-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="20e78-121">Protocol specifications</span></span>

<span data-ttu-id="20e78-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="20e78-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20e78-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-125">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="20e78-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="20e78-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-127">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="20e78-127">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="20e78-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-128">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-129">Trata a comunicação do cliente com um servidor de nome serviço provedor NSPI (Interface).</span><span class="sxs-lookup"><span data-stu-id="20e78-129">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
<span data-ttu-id="20e78-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-130">[[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-131">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="20e78-131">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="20e78-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-132">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-133">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="20e78-133">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="20e78-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-134">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-135">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="20e78-135">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="20e78-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-136">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-137">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="20e78-137">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="20e78-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-138">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-139">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="20e78-139">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="20e78-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-140">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-141">Especifica as propriedades e operações que são permitidas para modelos de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="20e78-141">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="20e78-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-142">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-143">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="20e78-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="20e78-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-144">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-145">Manipula mensagens de email de entrada em um servidor.</span><span class="sxs-lookup"><span data-stu-id="20e78-145">Manipulates incoming email messages on a server.</span></span>
    
<span data-ttu-id="20e78-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20e78-146">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20e78-147">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="20e78-147">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20e78-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20e78-148">Header files</span></span>

<span data-ttu-id="20e78-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20e78-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="20e78-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="20e78-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="20e78-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20e78-151">Mapitags.h</span></span>
  
> <span data-ttu-id="20e78-152">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="20e78-152">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20e78-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="20e78-153">See also</span></span>



[<span data-ttu-id="20e78-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20e78-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20e78-155">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="20e78-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20e78-156">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="20e78-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20e78-157">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="20e78-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
  
[<span data-ttu-id="20e78-158">Tipos de endereço MAPI</span><span class="sxs-lookup"><span data-stu-id="20e78-158">MAPI Address Types</span></span>](mapi-address-types.md)

