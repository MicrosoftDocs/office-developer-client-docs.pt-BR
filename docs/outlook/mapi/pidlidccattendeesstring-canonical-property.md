---
title: Propriedade canônica PidLidCcAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344965"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="90b24-103">Propriedade canônica PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="90b24-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="90b24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90b24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90b24-105">Contém uma lista de todos os participantes que podem ser enviados que também são participantes opcionais.</span><span class="sxs-lookup"><span data-stu-id="90b24-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90b24-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="90b24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90b24-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="90b24-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="90b24-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="90b24-108">Property set:</span></span>  <br/> |<span data-ttu-id="90b24-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="90b24-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="90b24-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="90b24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="90b24-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="90b24-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="90b24-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="90b24-112">Data type:</span></span>  <br/> |<span data-ttu-id="90b24-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="90b24-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="90b24-114">Área:</span><span class="sxs-lookup"><span data-stu-id="90b24-114">Area:</span></span>  <br/> |<span data-ttu-id="90b24-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="90b24-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90b24-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="90b24-116">Remarks</span></span>

<span data-ttu-id="90b24-117">O valor de cada participante é a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do catálogo de endereços do participante.</span><span class="sxs-lookup"><span data-stu-id="90b24-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="90b24-118">Entradas separadas devem ser delimitadas por ponto-e-vírgula seguido por um espaço.</span><span class="sxs-lookup"><span data-stu-id="90b24-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="90b24-119">Esta propriedade não é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="90b24-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90b24-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="90b24-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90b24-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="90b24-121">Protocol specifications</span></span>

<span data-ttu-id="90b24-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90b24-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90b24-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="90b24-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90b24-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90b24-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90b24-125">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="90b24-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="90b24-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90b24-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90b24-127">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="90b24-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90b24-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="90b24-128">Header files</span></span>

<span data-ttu-id="90b24-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="90b24-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="90b24-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="90b24-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90b24-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="90b24-131">See also</span></span>



[<span data-ttu-id="90b24-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="90b24-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90b24-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="90b24-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90b24-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="90b24-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90b24-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="90b24-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

