---
title: Propriedade canônica PidTagEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmailAddress
api_type:
- HeaderDef
ms.assetid: bbd1e187-172e-4612-9efe-7c8e52967dfe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f70d5fbe9a52c491d5db668f541ce317f2675c6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569040"
---
# <a name="pidtagemailaddress-canonical-property"></a><span data-ttu-id="1dcf4-103">Propriedade canônica PidTagEmailAddress</span><span class="sxs-lookup"><span data-stu-id="1dcf4-103">PidTagEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="1dcf4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dcf4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dcf4-105">Contém o endereço de email de mensagens do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-105">Contains the messaging user's email address.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1dcf4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1dcf4-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1dcf4-107">PR_EMAIL_ADDRESS, PR_EMAIL_ADDRESS_A, PR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="1dcf4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1dcf4-109">0x3003</span><span class="sxs-lookup"><span data-stu-id="1dcf4-109">0x3003</span></span>  <br/> |
|<span data-ttu-id="1dcf4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-110">Data type:</span></span>  <br/> |<span data-ttu-id="1dcf4-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1dcf4-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1dcf4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-112">Area:</span></span>  <br/> |<span data-ttu-id="1dcf4-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="1dcf4-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dcf4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dcf4-114">Remarks</span></span>

<span data-ttu-id="1dcf4-115">Essas propriedades são exemplos das propriedades de um endereço base para todos os usuários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-115">These properties are examples of the base address properties for all messaging users.</span></span> <span data-ttu-id="1dcf4-116">É uma cadeia de caracteres terminada em nulo, cujo formato tem significado apenas para o sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-116">It is a null-terminated string whose format has meaning only for the underlying messaging system.</span></span> 
  
<span data-ttu-id="1dcf4-117">Essas propriedades são usadas em conjunto com as propriedades de **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) no endereçamento de mensagens e o **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1dcf4-117">These properties are used in conjunction with the **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) properties in addressing messages.</span></span> <span data-ttu-id="1dcf4-118">O formato de cadeia de caracteres é qualificado pelo **PR_ADDRTYPE**.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-118">The string format is qualified by **PR_ADDRTYPE**.</span></span> 
  
<span data-ttu-id="1dcf4-119">Valores válidos para essa propriedade incluem:</span><span class="sxs-lookup"><span data-stu-id="1dcf4-119">Valid values for this property include:</span></span> 
  
```cpp
network/postoffice/user 
Bruce@XYZZY.COM 
/c=US/a=att/p=Microsoft/o=Finance/ou=Purchasing/s=Furthur/g=Joe 
 
```

## <a name="related-resources"></a><span data-ttu-id="1dcf4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dcf4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1dcf4-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1dcf4-121">Protocol specifications</span></span>

<span data-ttu-id="1dcf4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dcf4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dcf4-123">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1dcf4-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dcf4-124">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dcf4-125">Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-125">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="1dcf4-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dcf4-126">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dcf4-127">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-127">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1dcf4-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1dcf4-128">Header files</span></span>

<span data-ttu-id="1dcf4-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1dcf4-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1dcf4-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1dcf4-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1dcf4-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1dcf4-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1dcf4-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dcf4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dcf4-133">See also</span></span>



[<span data-ttu-id="1dcf4-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1dcf4-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1dcf4-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1dcf4-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1dcf4-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1dcf4-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1dcf4-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1dcf4-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

