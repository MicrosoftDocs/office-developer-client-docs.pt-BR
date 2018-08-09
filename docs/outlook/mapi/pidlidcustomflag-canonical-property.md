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
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768360"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="fb837-103">Propriedade canônica PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="fb837-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="fb837-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb837-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb837-105">Uma máscara de bits que especifica como uma mensagem é personalizada, por exemplo, salvo com propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="fb837-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="fb837-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fb837-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fb837-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="fb837-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="fb837-108">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="fb837-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fb837-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="fb837-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="fb837-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fb837-110">Data type:</span></span>  <br/> |<span data-ttu-id="fb837-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fb837-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb837-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb837-112">Remarks</span></span>

<span data-ttu-id="fb837-113">Para recuperar o valor dessa propriedade, primeiro use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** para obter a marca de propriedade e especifique nesta marca de propriedade em **[IMAPIProp::GetProps](imapiprop-getprops.md)** para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="fb837-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="fb837-114">Sinalizadores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="fb837-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="fb837-115">**Constante**</span><span class="sxs-lookup"><span data-stu-id="fb837-115">**Constant**</span></span>|<span data-ttu-id="fb837-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fb837-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb837-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="fb837-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="fb837-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="fb837-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="fb837-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="fb837-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="fb837-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="fb837-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="fb837-121">Ao chamar **IMAPIProp::GetIDsFromNames**, especifique os seguintes valores para a estrutura **[MAPINAMEID](mapinameid.md)** apontado pelo parâmetro de entrada *lppPropNames* .</span><span class="sxs-lookup"><span data-stu-id="fb837-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="fb837-122">**Membro**</span><span class="sxs-lookup"><span data-stu-id="fb837-122">**Member**</span></span>|<span data-ttu-id="fb837-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fb837-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb837-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="fb837-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="fb837-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fb837-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fb837-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="fb837-126">ulKind:</span></span>  <br/> |<span data-ttu-id="fb837-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="fb837-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="fb837-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="fb837-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="fb837-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="fb837-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="fb837-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fb837-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fb837-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fb837-131">Protocol specifications</span></span>

<span data-ttu-id="fb837-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fb837-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fb837-133">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb837-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fb837-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fb837-134">Header files</span></span>

<span data-ttu-id="fb837-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fb837-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="fb837-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fb837-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="fb837-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fb837-137">Mapitags.h</span></span>
  
> <span data-ttu-id="fb837-138">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fb837-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb837-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb837-139">See also</span></span>



[<span data-ttu-id="fb837-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fb837-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fb837-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fb837-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fb837-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fb837-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fb837-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fb837-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

