---
title: Propriedade canônica PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338070"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a><span data-ttu-id="fe860-103">Propriedade canônica PidLidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="fe860-103">PidLidEmail3OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="fe860-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe860-105">Especifica o terceiro nome para exibição que corresponde ao endereço de email especificado para o contato.</span><span class="sxs-lookup"><span data-stu-id="fe860-105">Specifies the third display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe860-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fe860-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe860-107">dispidEmail3OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="fe860-107">dispidEmail3OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="fe860-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="fe860-108">Property set:</span></span>  <br/> |<span data-ttu-id="fe860-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="fe860-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="fe860-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fe860-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fe860-111">0x000080A4</span><span class="sxs-lookup"><span data-stu-id="fe860-111">0x000080A4</span></span>  <br/> |
|<span data-ttu-id="fe860-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fe860-112">Data type:</span></span>  <br/> |<span data-ttu-id="fe860-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fe860-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fe860-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fe860-114">Area:</span></span>  <br/> |<span data-ttu-id="fe860-115">Contato</span><span class="sxs-lookup"><span data-stu-id="fe860-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe860-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe860-116">Remarks</span></span>

<span data-ttu-id="fe860-117">Se o valor da propriedade **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) for "SMTP", o valor da respectiva **propriedade dispidEmail3OriginalDisplayName** deve ser igual ao valor do respectivo **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fe860-117">If the value of the **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail3OriginalDisplayName** property should equal the value of the respective **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)).</span></span> <span data-ttu-id="fe860-118">O objetivo dessa propriedade é exibir um endereço amigável alternativo que seja equivalente ao endereço no **dispidEmail3EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="fe860-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail3EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe860-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe860-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe860-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fe860-120">Protocol specifications</span></span>

<span data-ttu-id="fe860-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe860-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe860-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fe860-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fe860-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe860-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe860-124">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="fe860-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe860-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="fe860-125">Header files</span></span>

<span data-ttu-id="fe860-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe860-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe860-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fe860-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe860-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe860-128">See also</span></span>



[<span data-ttu-id="fe860-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe860-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe860-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fe860-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe860-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe860-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe860-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fe860-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

