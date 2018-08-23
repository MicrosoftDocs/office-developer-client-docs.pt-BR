---
title: Propriedade canônica PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: beb2c46b43ae77de08900aeb987d875e85575aba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563181"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a><span data-ttu-id="f0871-103">Propriedade canônica PidLidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="f0871-103">PidLidSharingResponseType Canonical Property</span></span>

  
  
<span data-ttu-id="f0871-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0871-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0871-105">Especifica o tipo de resposta com a qual o destinatário da solicitação de compartilhamento respondido.</span><span class="sxs-lookup"><span data-stu-id="f0871-105">Specifies the type of response with which the recipient of the sharing request responded.</span></span> <span data-ttu-id="f0871-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f0871-106">This is a property of a sharing message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0871-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f0871-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="f0871-108">dispidSharingResponseType</span><span class="sxs-lookup"><span data-stu-id="f0871-108">dispidSharingResponseType</span></span>  <br/> |
|<span data-ttu-id="f0871-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="f0871-109">Property set:</span></span>  <br/> |<span data-ttu-id="f0871-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="f0871-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="f0871-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="f0871-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f0871-112">0x00008A27</span><span class="sxs-lookup"><span data-stu-id="f0871-112">0x00008A27</span></span>  <br/> |
|<span data-ttu-id="f0871-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f0871-113">Data type:</span></span>  <br/> |<span data-ttu-id="f0871-114">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f0871-114">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f0871-115">Área:</span><span class="sxs-lookup"><span data-stu-id="f0871-115">Area:</span></span>  <br/> |<span data-ttu-id="f0871-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="f0871-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0871-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0871-117">Remarks</span></span>

<span data-ttu-id="f0871-118">O valor dessa propriedade deve ser definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f0871-118">The value of this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="f0871-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f0871-119">**Value**</span></span>|<span data-ttu-id="f0871-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0871-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f0871-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0871-121">0x00000000</span></span>  <br/> |<span data-ttu-id="f0871-122">Nenhuma resposta</span><span class="sxs-lookup"><span data-stu-id="f0871-122">No response</span></span>  <br/> |
|<span data-ttu-id="f0871-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f0871-123">0x00000001</span></span>  <br/> |<span data-ttu-id="f0871-124">Aceito</span><span class="sxs-lookup"><span data-stu-id="f0871-124">Accepted</span></span>  <br/> |
|<span data-ttu-id="f0871-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f0871-125">0x00000002</span></span>  <br/> |<span data-ttu-id="f0871-126">Negado</span><span class="sxs-lookup"><span data-stu-id="f0871-126">Denied</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f0871-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0871-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f0871-128">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f0871-128">Protocol specifications</span></span>

<span data-ttu-id="f0871-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0871-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0871-130">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f0871-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f0871-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f0871-131">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f0871-132">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="f0871-132">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f0871-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f0871-133">Header files</span></span>

<span data-ttu-id="f0871-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0871-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f0871-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f0871-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0871-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0871-136">See also</span></span>



[<span data-ttu-id="f0871-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f0871-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f0871-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f0871-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f0871-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f0871-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f0871-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f0871-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

