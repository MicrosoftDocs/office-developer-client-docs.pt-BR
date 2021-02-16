---
title: Propriedade canônica PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7fb7e5afa6a1c050a5d91274bc4f82439fb98640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337958"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="ceb53-103">Propriedade canônica PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ceb53-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="ceb53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ceb53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ceb53-105">Especifica o segundo nome para exibição que corresponde ao endereço de email especificado para o contato.</span><span class="sxs-lookup"><span data-stu-id="ceb53-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ceb53-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ceb53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ceb53-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="ceb53-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="ceb53-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ceb53-108">Property set:</span></span>  <br/> |<span data-ttu-id="ceb53-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ceb53-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ceb53-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ceb53-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ceb53-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="ceb53-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="ceb53-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ceb53-112">Data type:</span></span>  <br/> |<span data-ttu-id="ceb53-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ceb53-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ceb53-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ceb53-114">Area:</span></span>  <br/> |<span data-ttu-id="ceb53-115">Contato</span><span class="sxs-lookup"><span data-stu-id="ceb53-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ceb53-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceb53-116">Remarks</span></span>

<span data-ttu-id="ceb53-117">Se o valor da propriedade **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) for "SMTP", o valor da respectiva propriedade **PidLidEmail2OriginalDisplayName** deve ser igual ao valor da respectiva propriedade **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ceb53-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="ceb53-118">O objetivo dessa propriedade é exibir um endereço amigável alternativo que seja equivalente ao endereço no **dispidEmail2EmailAddress**.</span><span class="sxs-lookup"><span data-stu-id="ceb53-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ceb53-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ceb53-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ceb53-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ceb53-120">Protocol specifications</span></span>

<span data-ttu-id="ceb53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ceb53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ceb53-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ceb53-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ceb53-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ceb53-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ceb53-124">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="ceb53-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ceb53-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ceb53-125">Header files</span></span>

<span data-ttu-id="ceb53-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ceb53-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ceb53-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ceb53-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ceb53-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceb53-128">See also</span></span>



[<span data-ttu-id="ceb53-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ceb53-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ceb53-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ceb53-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ceb53-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ceb53-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ceb53-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ceb53-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

