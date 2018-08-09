---
title: Propriedade canônica PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 86ef98ac7b4084de3a96210298fe0d5509d12103
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768314"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="4137f-103">Propriedade canônica PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="4137f-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="4137f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4137f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4137f-105">Especifica as opções que são usadas no processamento automático de mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="4137f-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4137f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4137f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4137f-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="4137f-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="4137f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4137f-108">Property set:</span></span>  <br/> |<span data-ttu-id="4137f-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4137f-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4137f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4137f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4137f-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="4137f-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="4137f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4137f-112">Data type:</span></span>  <br/> |<span data-ttu-id="4137f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4137f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4137f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4137f-114">Area:</span></span>  <br/> |<span data-ttu-id="4137f-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="4137f-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4137f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4137f-116">Remarks</span></span>

<span data-ttu-id="4137f-117">A propriedade pode ser ausente, caso em que o valor padrão de "0x00000000" é usado.</span><span class="sxs-lookup"><span data-stu-id="4137f-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="4137f-118">Se definido, essa propriedade deverá ser definida como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4137f-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="4137f-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4137f-119">**Value**</span></span>|<span data-ttu-id="4137f-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4137f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4137f-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4137f-121">0x00000000</span></span>  <br/> |<span data-ttu-id="4137f-122">Automaticamente não processe a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4137f-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="4137f-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4137f-123">0x00000001</span></span>  <br/> |<span data-ttu-id="4137f-124">Processar a mensagem automaticamente ou quando a mensagem é aberta.</span><span class="sxs-lookup"><span data-stu-id="4137f-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="4137f-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4137f-125">0x00000002</span></span>  <br/> |<span data-ttu-id="4137f-126">Processe a mensagem somente quando a mensagem é aberta.</span><span class="sxs-lookup"><span data-stu-id="4137f-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4137f-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4137f-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4137f-128">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4137f-128">Protocol specifications</span></span>

<span data-ttu-id="4137f-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4137f-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4137f-130">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4137f-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4137f-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4137f-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4137f-132">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4137f-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4137f-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4137f-133">Header files</span></span>

<span data-ttu-id="4137f-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4137f-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="4137f-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4137f-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4137f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4137f-136">See also</span></span>



[<span data-ttu-id="4137f-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4137f-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4137f-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4137f-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4137f-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4137f-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4137f-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4137f-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

