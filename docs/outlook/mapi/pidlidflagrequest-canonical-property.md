---
title: Propriedade canônico de PidLidFlagRequest
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768466"
---
# <a name="pidlidflagrequest-canonical-property"></a><span data-ttu-id="31055-103">Propriedade canônico de PidLidFlagRequest</span><span class="sxs-lookup"><span data-stu-id="31055-103">PidLidFlagRequest Canonical Property</span></span>

  
  
<span data-ttu-id="31055-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31055-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31055-105">Representa o status de uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="31055-105">Represents the status of a meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31055-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="31055-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31055-107">dispidRequest</span><span class="sxs-lookup"><span data-stu-id="31055-107">dispidRequest</span></span>  <br/> |
|<span data-ttu-id="31055-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="31055-108">Property set:</span></span>  <br/> |<span data-ttu-id="31055-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="31055-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="31055-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="31055-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="31055-111">0x00008530</span><span class="sxs-lookup"><span data-stu-id="31055-111">0x00008530</span></span>  <br/> |
|<span data-ttu-id="31055-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="31055-112">Data type:</span></span>  <br/> |<span data-ttu-id="31055-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="31055-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="31055-114">Área:</span><span class="sxs-lookup"><span data-stu-id="31055-114">Area:</span></span>  <br/> |<span data-ttu-id="31055-115">Sinalizando</span><span class="sxs-lookup"><span data-stu-id="31055-115">Flagging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31055-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="31055-116">Remarks</span></span>

<span data-ttu-id="31055-117">No Microsoft Office Outlook, uma solicitação de reunião é um item de compromisso.</span><span class="sxs-lookup"><span data-stu-id="31055-117">In Microsoft Office Outlook, a meeting request is an appointment item.</span></span>
  
<span data-ttu-id="31055-118">Essa propriedade contém texto especificáveis de usuário a ser associado com o sinalizador e deve ser definida se o objeto de mensagem foi sinalizado ou concluído, mas não deve existir para um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="31055-118">This property contains user-specifiable text to be associated with the flag and should be set if the message object is flagged or completed, but should not exist for a meeting-related object.</span></span> <span data-ttu-id="31055-119">Os clientes podem optar por não suporte para essa propriedade e sempre escrever "Acompanhamento" (traduzido para o idioma do usuário, se apropriado) como o valor da cadeia de caracteres quando essa propriedade deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="31055-119">Clients may choose not to support this property, and always write "Follow up" (translated to the user's language if appropriate) as the value of the string when this property should be set.</span></span> <span data-ttu-id="31055-120">Esta propriedade deve ser ignorada condicionalmente com base nos valores das propriedades **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) e **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31055-120">This property should be conditionally ignored based on the values of the **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="31055-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="31055-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="31055-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="31055-122">Protocol specifications</span></span>

<span data-ttu-id="31055-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31055-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31055-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="31055-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="31055-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="31055-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="31055-126">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="31055-126">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="31055-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="31055-127">Header files</span></span>

<span data-ttu-id="31055-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31055-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="31055-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="31055-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31055-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="31055-130">See also</span></span>



[<span data-ttu-id="31055-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="31055-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31055-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="31055-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31055-133">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="31055-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31055-134">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="31055-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

