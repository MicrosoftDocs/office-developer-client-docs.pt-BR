---
title: Propriedade canônica PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357803"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="b01a4-103">Propriedade canônica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="b01a4-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="b01a4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b01a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b01a4-105">Representa o status de uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="b01a4-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b01a4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b01a4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b01a4-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="b01a4-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="b01a4-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b01a4-108">Property set:</span></span>  <br/> |<span data-ttu-id="b01a4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="b01a4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="b01a4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b01a4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b01a4-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="b01a4-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="b01a4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b01a4-112">Data type:</span></span>  <br/> |<span data-ttu-id="b01a4-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b01a4-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b01a4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b01a4-114">Area:</span></span>  <br/> |<span data-ttu-id="b01a4-115">Sinalização</span><span class="sxs-lookup"><span data-stu-id="b01a4-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b01a4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b01a4-116">Remarks</span></span>

<span data-ttu-id="b01a4-117">No Microsoft Office Outlook, uma solicitação de reunião é um item de compromisso.</span><span class="sxs-lookup"><span data-stu-id="b01a4-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="b01a4-118">Essa propriedade contém texto especificado pelo usuário a ser associado ao sinalizador e deve ser definida se o objeto de mensagem estiver sinalizado ou concluído, mas não deve existir para um objeto relacionado à reunião.</span><span class="sxs-lookup"><span data-stu-id="b01a4-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="b01a4-119">Os clientes podem optar por não dar suporte a essa propriedade e sempre escrever "Acompanhamento" (traduzido para o idioma do usuário, se apropriado) como o valor da cadeia de caracteres quando essa propriedade deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="b01a4-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="b01a4-120">Essa propriedade deve ser ignorada condicionalmente com base nos valores das propriedades **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b01a4-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b01a4-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b01a4-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b01a4-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b01a4-122">Protocol specifications</span></span>

<span data-ttu-id="b01a4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b01a4-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b01a4-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b01a4-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b01a4-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b01a4-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b01a4-126">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="b01a4-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b01a4-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b01a4-127">Header files</span></span>

<span data-ttu-id="b01a4-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b01a4-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b01a4-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b01a4-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b01a4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b01a4-130">See also</span></span>



[<span data-ttu-id="b01a4-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b01a4-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b01a4-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b01a4-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b01a4-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b01a4-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b01a4-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b01a4-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

