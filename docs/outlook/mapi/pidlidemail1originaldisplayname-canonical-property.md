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
ms.openlocfilehash: 7d09830f471fbaa0e8ed6ae70420dfea6428b9df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768382"
---
# <a name="pidlidemail1originaldisplayname-canonical-property"></a><span data-ttu-id="079f7-103">Propriedade canônica PidLidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="079f7-103">PidLidEmail1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="079f7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="079f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="079f7-105">Especifica o primeiro nome de exibição que corresponde ao endereço de email especificado para o contato.</span><span class="sxs-lookup"><span data-stu-id="079f7-105">Specifies the first display name that corresponds to the email address that is specified for the contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="079f7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="079f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="079f7-107">dispidEmail1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="079f7-107">dispidEmail1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="079f7-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="079f7-108">Property set:</span></span>  <br/> |<span data-ttu-id="079f7-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="079f7-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="079f7-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="079f7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="079f7-111">0x00008084</span><span class="sxs-lookup"><span data-stu-id="079f7-111">0x00008084</span></span>  <br/> |
|<span data-ttu-id="079f7-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="079f7-112">Data type:</span></span>  <br/> |<span data-ttu-id="079f7-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="079f7-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="079f7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="079f7-114">Area:</span></span>  <br/> |<span data-ttu-id="079f7-115">Contato</span><span class="sxs-lookup"><span data-stu-id="079f7-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="079f7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="079f7-116">Remarks</span></span>

<span data-ttu-id="079f7-117">Se o valor da propriedade **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) for "SMTP", o valor da propriedade respectivos **dispidEmail1OriginalDisplayName** será igual ao valor de **os respectivos dispidEmail1EmailAddress** propriedade ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="079f7-117">If the value of the **dispidEmail1AddrType** ([PidLidEmail1AddressType](pidlidemail1addresstype-canonical-property.md)) property is "SMTP", the value of the respective **dispidEmail1OriginalDisplayName** property should equal the value of the respective **dispidEmail1EmailAddress** ([PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="079f7-118">Essa propriedade exibirá um endereço alternativo de fácil utilização que é equivalente na propriedade **dispidEmail1EmailAddress** .</span><span class="sxs-lookup"><span data-stu-id="079f7-118">This property displays an alternative user-friendly address that is equivalent to the one in the **dispidEmail1EmailAddress** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="079f7-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="079f7-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="079f7-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="079f7-120">Protocol specifications</span></span>

<span data-ttu-id="079f7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="079f7-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="079f7-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="079f7-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="079f7-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="079f7-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="079f7-124">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="079f7-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="079f7-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="079f7-125">Header files</span></span>

<span data-ttu-id="079f7-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="079f7-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="079f7-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="079f7-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="079f7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="079f7-128">See also</span></span>



[<span data-ttu-id="079f7-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="079f7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="079f7-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="079f7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="079f7-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="079f7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="079f7-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="079f7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

