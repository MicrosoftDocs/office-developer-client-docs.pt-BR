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
ms.openlocfilehash: 2b3f59633fcea0b895cd024dbbbc106c8d492bf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768373"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a><span data-ttu-id="12646-103">Propriedade canônica PidLidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="12646-103">PidLidEmail2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="12646-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12646-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12646-105">Especifica o nome de exibição segundo que corresponde ao endereço de email especificado para o contato.</span><span class="sxs-lookup"><span data-stu-id="12646-105">Specifies the second display name that corresponds to the email address specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12646-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="12646-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12646-107">dispidEmail2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="12646-107">dispidEmail2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="12646-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="12646-108">Property set:</span></span>  <br/> |<span data-ttu-id="12646-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="12646-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="12646-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="12646-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="12646-111">0x00008094</span><span class="sxs-lookup"><span data-stu-id="12646-111">0x00008094</span></span>  <br/> |
|<span data-ttu-id="12646-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="12646-112">Data type:</span></span>  <br/> |<span data-ttu-id="12646-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12646-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="12646-114">Área:</span><span class="sxs-lookup"><span data-stu-id="12646-114">Area:</span></span>  <br/> |<span data-ttu-id="12646-115">Contato</span><span class="sxs-lookup"><span data-stu-id="12646-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12646-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="12646-116">Remarks</span></span>

<span data-ttu-id="12646-117">Se o valor da propriedade **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) for "SMTP", o valor da propriedade **PidLidEmail2OriginalDisplayName** respectivo será igual ao valor de **os respectivos dispidEmail2EmailAddress** propriedade ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="12646-117">If the value of the **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) property is "SMTP", the value of the respective **PidLidEmail2OriginalDisplayName** property should equal the value of the respective **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="12646-118">A finalidade dessa propriedade é para exibir um endereço alternativo de fácil utilização que é equivalente ao **dispidEmail2EmailAddress**especificado no.</span><span class="sxs-lookup"><span data-stu-id="12646-118">The purpose of this property is to display an alternative user-friendly address that is equivalent to the one in the **dispidEmail2EmailAddress**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="12646-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="12646-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12646-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="12646-120">Protocol specifications</span></span>

<span data-ttu-id="12646-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12646-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12646-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="12646-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12646-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12646-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12646-124">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="12646-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12646-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12646-125">Header files</span></span>

<span data-ttu-id="12646-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12646-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="12646-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="12646-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12646-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="12646-128">See also</span></span>



[<span data-ttu-id="12646-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="12646-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12646-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="12646-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12646-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="12646-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12646-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="12646-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
