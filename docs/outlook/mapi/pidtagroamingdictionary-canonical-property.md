---
title: Propriedade canônica PidTagRoamingDictionary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDictionary
api_type:
- COM
ms.assetid: 40b50181-f88c-40ee-b3d0-a36dd36c158e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 41d1a4abe79892fa1c9c8789e159a19645318497
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769872"
---
# <a name="pidtagroamingdictionary-canonical-property"></a><span data-ttu-id="261f3-103">Propriedade canônica PidTagRoamingDictionary</span><span class="sxs-lookup"><span data-stu-id="261f3-103">PidTagRoamingDictionary Canonical Property</span></span>

<span data-ttu-id="261f3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="261f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="261f3-105">Contém um documento XML que descreve o dicionário de roaming.</span><span class="sxs-lookup"><span data-stu-id="261f3-105">Contains an XML document that describes the roaming dictionary.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="261f3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="261f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="261f3-107">PR_ROAMING_DICTIONARY</span><span class="sxs-lookup"><span data-stu-id="261f3-107">PR_ROAMING_DICTIONARY</span></span>  <br/> |
|<span data-ttu-id="261f3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="261f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="261f3-109">0x7C07</span><span class="sxs-lookup"><span data-stu-id="261f3-109">0x7C07</span></span>  <br/> |
|<span data-ttu-id="261f3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="261f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="261f3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="261f3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="261f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="261f3-112">Area:</span></span>  <br/> |<span data-ttu-id="261f3-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="261f3-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="261f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="261f3-114">Remarks</span></span>

<span data-ttu-id="261f3-115">Essa propriedade contém um documento de UNICODE XML que está usando a codificação UTF8.</span><span class="sxs-lookup"><span data-stu-id="261f3-115">This property contains a UNICODE XML document that is using UTF8 encoding.</span></span> <span data-ttu-id="261f3-116">Uma mensagem com um fluxo de dicionário deve definir esta propriedade com o esquema a seguir:</span><span class="sxs-lookup"><span data-stu-id="261f3-116">A message with a dictionary stream must set this property with the following schema:</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?> 
<xs:schema targetNamespace="Dictionary.xsd" xmlns="Dictionary.xsd" xmlns:xs="http://www.w3.org/2001/XMLSchema"> 
   <xs:element name="UserConfiguration"> 
   <xs:complexType> 
   <xs:sequence> 
   <xs:element name="Info"> 
   <xs:complexType> 
   <xs:sequence /> 
   <xs:attribute name="version" type="VersionString"> 
   </xs:attribute> 
   </xs:complexType>
```

<span data-ttu-id="261f3-117">Este é um documento XML de exemplo armazenado nessa propriedade em uma mensagem de dados de configuração:</span><span class="sxs-lookup"><span data-stu-id="261f3-117">The following is a sample XML document stored in this property on a Configuration Data message:</span></span> 
  
```xml
<?xml version="1.0"?> 
<UserConfiguration> 
<Info version="Outlook.12"/> 
<Data> <e k="18-piAutoProcess" v="3-True"/> 
<e k="18-piRemindDefault" v="9-15"/> 
<e k="18-piReminderUpgradeTime" v="9-212864507"/> 
<e k="18-OLPrefsVersion" v="9-1"/> 
</Data> 
</UserConfiguration>
```

## <a name="related-resources"></a><span data-ttu-id="261f3-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="261f3-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="261f3-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="261f3-119">Protocol specifications</span></span>

<span data-ttu-id="261f3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="261f3-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="261f3-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="261f3-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="261f3-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="261f3-122">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="261f3-123">Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="261f3-123">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="261f3-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="261f3-124">Header files</span></span>

<span data-ttu-id="261f3-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="261f3-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="261f3-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="261f3-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="261f3-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="261f3-127">Mapitags.h</span></span>
  
> <span data-ttu-id="261f3-128">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="261f3-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="261f3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="261f3-129">See also</span></span>



[<span data-ttu-id="261f3-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="261f3-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="261f3-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="261f3-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="261f3-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="261f3-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="261f3-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="261f3-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
