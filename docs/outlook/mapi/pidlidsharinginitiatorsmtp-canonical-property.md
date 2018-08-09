---
title: Propriedade canônica PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 188424fc67534ea5df6ed5eb209909731e12c73c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768655"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="2e24e-103">Propriedade canônica PidLidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2e24e-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="2e24e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e24e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e24e-105">Especifica o endereço SMTP do usuário que iniciou a mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2e24e-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="2e24e-106">Esta é uma propriedade de uma mensagem de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2e24e-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2e24e-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2e24e-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="2e24e-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="2e24e-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="2e24e-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="2e24e-109">Property set:</span></span>  <br/> |<span data-ttu-id="2e24e-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="2e24e-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="2e24e-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="2e24e-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2e24e-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="2e24e-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="2e24e-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2e24e-113">Data type:</span></span>  <br/> |<span data-ttu-id="2e24e-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e24e-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e24e-115">Área:</span><span class="sxs-lookup"><span data-stu-id="2e24e-115">Area:</span></span>  <br/> |<span data-ttu-id="2e24e-116">Sharing</span><span class="sxs-lookup"><span data-stu-id="2e24e-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e24e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e24e-117">Remarks</span></span>

<span data-ttu-id="2e24e-118">Esta propriedade deve ser definida com o valor da propriedade **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) do catálogo de endereços identificado pela propriedade **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) e deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="2e24e-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2e24e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e24e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2e24e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2e24e-120">Protocol specifications</span></span>

<span data-ttu-id="2e24e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e24e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e24e-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e24e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2e24e-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2e24e-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2e24e-124">Compartilha pastas de caixa de correio entre clientes.</span><span class="sxs-lookup"><span data-stu-id="2e24e-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2e24e-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2e24e-125">Header files</span></span>

<span data-ttu-id="2e24e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2e24e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2e24e-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2e24e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2e24e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e24e-128">See also</span></span>



[<span data-ttu-id="2e24e-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2e24e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2e24e-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2e24e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2e24e-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2e24e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2e24e-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2e24e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

