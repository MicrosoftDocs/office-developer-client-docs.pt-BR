---
title: Propriedade canônica PidLidEmail1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail1OriginalDisplayName
api_type:
- COM
ms.assetid: 991c2969-0180-4c7d-95ee-e62fd24d67ef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a20ae8e3f19073bfb88d58db516a0e5f93d91445
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335039"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="7d2f9-103">Propriedade canônica PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="7d2f9-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="7d2f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d2f9-105">Especifica o primeiro nome para exibição que corresponde ao endereço de email especificado para o contato.</span><span class="sxs-lookup"><span data-stu-id="7d2f9-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d2f9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7d2f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d2f9-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="7d2f9-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="7d2f9-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="7d2f9-108">Property set:</span></span>  <br/> |<span data-ttu-id="7d2f9-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7d2f9-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7d2f9-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7d2f9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7d2f9-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="7d2f9-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="7d2f9-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7d2f9-112">Data type:</span></span>  <br/> |<span data-ttu-id="7d2f9-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7d2f9-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7d2f9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7d2f9-114">Area:</span></span>  <br/> |<span data-ttu-id="7d2f9-115">Contato</span><span class="sxs-lookup"><span data-stu-id="7d2f9-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d2f9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d2f9-116">Remarks</span></span>

<span data-ttu-id="7d2f9-117">Se o valor da propriedade **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) for "SMTP", o valor da respectiva **propriedade dispidEmail1OriginalDisplayName** deve ser igual ao valor da respectiva propriedade **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7d2f9-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="7d2f9-118">Essa propriedade exibe um endereço amigável alternativo que é equivalente ao endereço da propriedade **dispidEmail1EmailAddress.**</span><span class="sxs-lookup"><span data-stu-id="7d2f9-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d2f9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d2f9-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d2f9-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d2f9-120">Protocol specifications</span></span>

<span data-ttu-id="7d2f9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2f9-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2f9-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7d2f9-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d2f9-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2f9-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2f9-124">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="7d2f9-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d2f9-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7d2f9-125">Header files</span></span>

<span data-ttu-id="7d2f9-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d2f9-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d2f9-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7d2f9-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d2f9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d2f9-128">See also</span></span>



[<span data-ttu-id="7d2f9-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2f9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d2f9-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2f9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d2f9-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d2f9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d2f9-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7d2f9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

