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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397363"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="f4d55-103">Propriedade canônica PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="f4d55-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="f4d55-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4d55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4d55-105">Representa o status de uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="f4d55-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f4d55-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f4d55-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4d55-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="f4d55-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="f4d55-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="f4d55-108">Property set:</span></span>  <br/> |<span data-ttu-id="f4d55-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f4d55-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f4d55-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="f4d55-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f4d55-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="f4d55-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="f4d55-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f4d55-112">Data type:</span></span>  <br/> |<span data-ttu-id="f4d55-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4d55-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4d55-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f4d55-114">Area:</span></span>  <br/> |<span data-ttu-id="f4d55-115">Sinalizando</span><span class="sxs-lookup"><span data-stu-id="f4d55-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4d55-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4d55-116">Remarks</span></span>

<span data-ttu-id="f4d55-117">No Microsoft Office Outlook, uma solicitação de reunião é um item de compromisso.</span><span class="sxs-lookup"><span data-stu-id="f4d55-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="f4d55-118">Essa propriedade contém texto especificáveis de usuário a ser associado com o sinalizador e deve ser definida se o objeto de mensagem foi sinalizado ou concluído, mas não deve existir para um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="f4d55-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="f4d55-119">Os clientes podem optar por não suporte para essa propriedade e sempre escrever "Acompanhamento" (traduzido para o idioma do usuário, se apropriado) como o valor da cadeia de caracteres quando essa propriedade deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="f4d55-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="f4d55-120">Esta propriedade deve ser ignorada condicionalmente com base nos valores das propriedades **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) e **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4d55-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f4d55-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4d55-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4d55-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f4d55-122">Protocol specifications</span></span>

<span data-ttu-id="f4d55-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d55-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d55-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f4d55-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4d55-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4d55-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4d55-126">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="f4d55-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4d55-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4d55-127">Header files</span></span>

<span data-ttu-id="f4d55-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4d55-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4d55-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f4d55-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4d55-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4d55-130">See also</span></span>



[<span data-ttu-id="f4d55-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d55-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4d55-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f4d55-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4d55-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f4d55-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4d55-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f4d55-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

