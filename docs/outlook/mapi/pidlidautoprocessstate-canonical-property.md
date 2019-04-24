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
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342060"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="4a536-103">Propriedade canônica PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="4a536-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="4a536-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a536-105">Especifica as opções usadas no processamento automático de mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="4a536-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a536-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4a536-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a536-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="4a536-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="4a536-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="4a536-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a536-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4a536-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4a536-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4a536-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a536-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="4a536-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="4a536-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4a536-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a536-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a536-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a536-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4a536-114">Area:</span></span>  <br/> |<span data-ttu-id="4a536-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="4a536-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a536-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a536-116">Remarks</span></span>

<span data-ttu-id="4a536-117">A propriedade pode estar ausente e, nesse caso, o valor padrão "0x00000000" é usado.</span><span class="sxs-lookup"><span data-stu-id="4a536-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="4a536-118">Se definido, esta propriedade deve ser definida como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4a536-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="4a536-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4a536-119">**Value**</span></span>|<span data-ttu-id="4a536-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4a536-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a536-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4a536-121">0x00000000</span></span>  <br/> |<span data-ttu-id="4a536-122">Não processa a mensagem automaticamente.</span><span class="sxs-lookup"><span data-stu-id="4a536-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="4a536-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a536-123">0x00000001</span></span>  <br/> |<span data-ttu-id="4a536-124">Processar a mensagem automaticamente ou quando a mensagem for aberta.</span><span class="sxs-lookup"><span data-stu-id="4a536-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="4a536-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4a536-125">0x00000002</span></span>  <br/> |<span data-ttu-id="4a536-126">Processa a mensagem somente quando a mensagem é aberta.</span><span class="sxs-lookup"><span data-stu-id="4a536-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4a536-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a536-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a536-128">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="4a536-128">Protocol specifications</span></span>

<span data-ttu-id="4a536-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a536-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a536-130">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4a536-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a536-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a536-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a536-132">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="4a536-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a536-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a536-133">Header files</span></span>

<span data-ttu-id="4a536-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4a536-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a536-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4a536-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a536-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a536-136">See also</span></span>



[<span data-ttu-id="4a536-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a536-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a536-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4a536-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a536-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4a536-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a536-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4a536-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

