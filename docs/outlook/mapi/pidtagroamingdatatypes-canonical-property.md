---
title: Propriedade canônica PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359553"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a><span data-ttu-id="9576a-103">Propriedade canônica PidTagRoamingDatatypes</span><span class="sxs-lookup"><span data-stu-id="9576a-103">PidTagRoamingDatatypes Canonical Property</span></span>

  
  
<span data-ttu-id="9576a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9576a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9576a-105">Contém uma máscara de bits que indica quais propriedades de fluxo existem na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9576a-105">Contains a bitmask that indicates which stream properties exist on the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9576a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9576a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9576a-107">PR_ROAMING_DATATYPES</span><span class="sxs-lookup"><span data-stu-id="9576a-107">PR_ROAMING_DATATYPES</span></span>  <br/> |
|<span data-ttu-id="9576a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="9576a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9576a-109">0x7C06</span><span class="sxs-lookup"><span data-stu-id="9576a-109">0x7C06</span></span>  <br/> |
|<span data-ttu-id="9576a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9576a-110">Data type:</span></span>  <br/> |<span data-ttu-id="9576a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9576a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9576a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="9576a-112">Area:</span></span>  <br/> |<span data-ttu-id="9576a-113">Configuração</span><span class="sxs-lookup"><span data-stu-id="9576a-113">Configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9576a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9576a-114">Remarks</span></span>

<span data-ttu-id="9576a-115">Essa propriedade deve ser definida como um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9576a-115">This property must be set to one or more of the following values:</span></span>
  
|<span data-ttu-id="9576a-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9576a-116">**Value**</span></span>|<span data-ttu-id="9576a-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9576a-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9576a-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9576a-118">0x00000002</span></span>  <br/> |<span data-ttu-id="9576a-119">Indica que a mensagem FAI (Informações Associadas à Pasta) deve conter um fluxo de dicionário, serializado em um esquema XML fixo e armazenado na propriedade **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9576a-119">Indicates that the Folder Associated Information (FAI) message should contain a Dictionary stream, serialized into a fixed XML schema and stored in the **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)) property.</span></span> <span data-ttu-id="9576a-120">Se a mensagem fai não contém um fluxo de dicionário, o aplicativo deve tratar o dicionário como não tendo entradas.</span><span class="sxs-lookup"><span data-stu-id="9576a-120">If the FAI message does not contain a Dictionary stream, the application must treat the Dictionary as having no entries.</span></span>  <br/> |
|<span data-ttu-id="9576a-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9576a-121">0x00000004</span></span>  <br/> |<span data-ttu-id="9576a-122">Indica que a mensagem FAI deve conter um fluxo XML armazenado na propriedade **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que usa um esquema XML arbitrário.</span><span class="sxs-lookup"><span data-stu-id="9576a-122">Indicates that the FAI message must contain an XML stream stored in the **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) property that uses an arbitrary XML schema.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="9576a-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9576a-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9576a-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9576a-124">Protocol specifications</span></span>

<span data-ttu-id="9576a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9576a-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9576a-126">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9576a-126">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9576a-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9576a-127">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9576a-128">Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9576a-128">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9576a-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9576a-129">Header files</span></span>

<span data-ttu-id="9576a-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9576a-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="9576a-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9576a-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="9576a-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9576a-132">Mapitags.h</span></span>
  
> <span data-ttu-id="9576a-133">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="9576a-133">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9576a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9576a-134">See also</span></span>



[<span data-ttu-id="9576a-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9576a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9576a-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9576a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9576a-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9576a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9576a-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9576a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

