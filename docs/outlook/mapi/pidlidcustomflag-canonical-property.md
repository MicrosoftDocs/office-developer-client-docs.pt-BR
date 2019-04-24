---
title: Propriedade canônica PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357614"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="bc068-103">Propriedade canônica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="bc068-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="bc068-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc068-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc068-105">Uma bitmask que especifica como uma mensagem é personalizada, por exemplo, salva com as propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bc068-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bc068-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bc068-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc068-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="bc068-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="bc068-108">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bc068-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bc068-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="bc068-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="bc068-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bc068-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc068-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bc068-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc068-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc068-112">Remarks</span></span>

<span data-ttu-id="bc068-113">Para recuperar o valor dessa propriedade, primeiro use **[IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md)** para obter a marca de propriedade e, em seguida, especifique essa marca de propriedade em **[IMAPIProp::](imapiprop-getprops.md)** GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="bc068-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="bc068-114">Os sinalizadores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="bc068-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="bc068-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="bc068-115">**Constant**</span></span>|<span data-ttu-id="bc068-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bc068-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc068-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="bc068-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="bc068-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="bc068-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="bc068-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="bc068-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="bc068-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="bc068-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="bc068-121">Ao chamar **IMAPIProp:: GetIDsFromNames**, especifique os seguintes valores para a estrutura **[MAPINAMEID](mapinameid.md)** apontada pelo parâmetro de entrada *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="bc068-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="bc068-122">**Member**</span><span class="sxs-lookup"><span data-stu-id="bc068-122">**Member**</span></span>|<span data-ttu-id="bc068-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bc068-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc068-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="bc068-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="bc068-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="bc068-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="bc068-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="bc068-126">ulKind:</span></span>  <br/> |<span data-ttu-id="bc068-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="bc068-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="bc068-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="bc068-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="bc068-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="bc068-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bc068-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc068-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bc068-131">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="bc068-131">Protocol specifications</span></span>

<span data-ttu-id="bc068-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc068-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bc068-133">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bc068-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bc068-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bc068-134">Header files</span></span>

<span data-ttu-id="bc068-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bc068-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc068-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bc068-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc068-137">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bc068-137">Mapitags.h</span></span>
  
> <span data-ttu-id="bc068-138">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="bc068-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc068-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc068-139">See also</span></span>



[<span data-ttu-id="bc068-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bc068-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc068-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bc068-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc068-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bc068-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc068-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bc068-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

