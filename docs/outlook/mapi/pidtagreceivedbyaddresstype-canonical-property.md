---
title: Propriedade canônica PidTagReceivedByAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedByAddressType
api_type:
- COM
ms.assetid: 0eef299d-6923-4dae-9a18-91ea82ea0f3e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00c07069ed174fe55556dfe48398d65b4e64100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359224"
---
# <a name="pidtagreceivedbyaddresstype-canonical-property"></a><span data-ttu-id="2b5fa-103">Propriedade canônica PidTagReceivedByAddressType</span><span class="sxs-lookup"><span data-stu-id="2b5fa-103">PidTagReceivedByAddressType Canonical Property</span></span>

  
  
<span data-ttu-id="2b5fa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b5fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b5fa-105">Contém o tipo de endereço de email, como SMTP, para o usuário de mensagens que realmente recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-105">Contains the email address type, such as SMTP, for the messaging user who actually receives the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2b5fa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2b5fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2b5fa-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="2b5fa-107">PR_RECEIVED_BY_ADDRTYPE, PR_RECEIVED_BY_ADDRTYPE_A, PR_RECEIVED_BY_ADDRTYPE_W</span></span>  <br/> |
|<span data-ttu-id="2b5fa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2b5fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2b5fa-109">0x0075</span><span class="sxs-lookup"><span data-stu-id="2b5fa-109">0x0075</span></span>  <br/> |
|<span data-ttu-id="2b5fa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2b5fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="2b5fa-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2b5fa-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2b5fa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2b5fa-112">Area:</span></span>  <br/> |<span data-ttu-id="2b5fa-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="2b5fa-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b5fa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b5fa-114">Remarks</span></span>

<span data-ttu-id="2b5fa-115">Essas propriedades são exemplos das propriedades de endereço do usuário de mensagens que realmente recebe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-115">These properties are examples of the address properties for the messaging user who actually receives the message.</span></span> <span data-ttu-id="2b5fa-116">Eles devem ser definidos pelo provedor de transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-116">They must be set by the incoming transport provider.</span></span>
  
<span data-ttu-id="2b5fa-117">A cadeia de caracteres de tipo de endereço pode conter apenas os caracteres alfabéticos maiúsculos a a Z e os números de zero a nove.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-117">The address type string can contain only the uppercase alphabetic characters A through Z and the numbers zero through nine.</span></span> <span data-ttu-id="2b5fa-118">Essas propriedades qualificam a propriedade **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) especificando um tipo de endereço, como SMTP, indicando como o endereço deve ser construído.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-118">These properties qualify the **PR_RECEIVED_BY_EMAIL_ADDRESS** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md)) property by specifying an address type, such as SMTP, thereby indicating how the address should be constructed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2b5fa-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b5fa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2b5fa-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="2b5fa-120">Protocol specifications</span></span>

<span data-ttu-id="2b5fa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b5fa-122">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2b5fa-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2b5fa-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2b5fa-124">Especifica as propriedades e as operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-124">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2b5fa-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2b5fa-125">Header files</span></span>

<span data-ttu-id="2b5fa-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="2b5fa-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2b5fa-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2b5fa-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="2b5fa-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2b5fa-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="2b5fa-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2b5fa-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b5fa-130">See also</span></span>



[<span data-ttu-id="2b5fa-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2b5fa-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2b5fa-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="2b5fa-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2b5fa-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2b5fa-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2b5fa-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2b5fa-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

