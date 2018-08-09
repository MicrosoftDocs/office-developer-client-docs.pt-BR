---
title: Propriedade canônica PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 148d71dc0e99e23ffe10445068170617cb26b01b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768841"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="2f09d-103">Propriedade canônica PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="2f09d-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="2f09d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2f09d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2f09d-105">Contém um valor de campo de cabeçalho Xref [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="2f09d-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2f09d-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="2f09d-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="2f09d-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2f09d-107">None</span></span>  <br/> |
|<span data-ttu-id="2f09d-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="2f09d-108">Property set:</span></span>  <br/> |<span data-ttu-id="2f09d-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="2f09d-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="2f09d-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="2f09d-110">Property name:</span></span>  <br/> |<span data-ttu-id="2f09d-111">XRef</span><span class="sxs-lookup"><span data-stu-id="2f09d-111">Xref</span></span>  <br/> |
|<span data-ttu-id="2f09d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2f09d-112">Data type:</span></span>  <br/> |<span data-ttu-id="2f09d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2f09d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2f09d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2f09d-114">Area:</span></span>  <br/> |<span data-ttu-id="2f09d-115">Email</span><span class="sxs-lookup"><span data-stu-id="2f09d-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f09d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f09d-116">Remarks</span></span>

<span data-ttu-id="2f09d-117">Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem escrever o valor desejado para um campo de cabeçalho XRef.</span><span class="sxs-lookup"><span data-stu-id="2f09d-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="2f09d-118">Leitores MIME devem copiar o valor de um campo de cabeçalho XRef com o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2f09d-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f09d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f09d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2f09d-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2f09d-120">Protocol specifications</span></span>

<span data-ttu-id="2f09d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f09d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f09d-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f09d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2f09d-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2f09d-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2f09d-124">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2f09d-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2f09d-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f09d-125">Header files</span></span>

<span data-ttu-id="2f09d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f09d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f09d-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2f09d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f09d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f09d-128">See also</span></span>



[<span data-ttu-id="2f09d-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2f09d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f09d-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2f09d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f09d-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2f09d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f09d-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2f09d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
