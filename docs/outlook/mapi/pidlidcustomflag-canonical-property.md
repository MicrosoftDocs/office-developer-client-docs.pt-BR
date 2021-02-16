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
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="179ae-103">Propriedade canônica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="179ae-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="179ae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="179ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="179ae-105">Uma máscara de bits que especifica como uma mensagem é personalizada, por exemplo, salva com propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="179ae-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="179ae-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="179ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="179ae-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="179ae-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="179ae-108">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="179ae-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="179ae-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="179ae-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="179ae-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="179ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="179ae-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="179ae-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="179ae-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="179ae-112">Remarks</span></span>

<span data-ttu-id="179ae-113">Para recuperar o valor dessa propriedade, primeiro use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obter a marca de propriedade e especifique essa marca de propriedade em **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="179ae-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="179ae-114">Os Sinalizadores possíveis são os seguinte:</span><span class="sxs-lookup"><span data-stu-id="179ae-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="179ae-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="179ae-115">**Constant**</span></span>|<span data-ttu-id="179ae-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="179ae-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="179ae-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="179ae-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="179ae-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="179ae-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="179ae-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="179ae-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="179ae-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="179ae-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="179ae-121">Ao chamar **IMAPIProp::GetIDsFromNames**, especifique os seguintes valores para a **[estrutura MAPINAMEID](mapinameid.md)** apontada pelo parâmetro de entrada  *lppPropNames*  .</span><span class="sxs-lookup"><span data-stu-id="179ae-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="179ae-122">**Membro**</span><span class="sxs-lookup"><span data-stu-id="179ae-122">**Member**</span></span>|<span data-ttu-id="179ae-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="179ae-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="179ae-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="179ae-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="179ae-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="179ae-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="179ae-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="179ae-126">ulKind:</span></span>  <br/> |<span data-ttu-id="179ae-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="179ae-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="179ae-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="179ae-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="179ae-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="179ae-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="179ae-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="179ae-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="179ae-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="179ae-131">Protocol specifications</span></span>

<span data-ttu-id="179ae-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="179ae-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="179ae-133">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="179ae-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="179ae-134">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="179ae-134">Header files</span></span>

<span data-ttu-id="179ae-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="179ae-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="179ae-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="179ae-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="179ae-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="179ae-137">Mapitags.h</span></span>
  
> <span data-ttu-id="179ae-138">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="179ae-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="179ae-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="179ae-139">See also</span></span>



[<span data-ttu-id="179ae-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="179ae-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="179ae-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="179ae-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="179ae-142">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="179ae-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="179ae-143">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="179ae-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

