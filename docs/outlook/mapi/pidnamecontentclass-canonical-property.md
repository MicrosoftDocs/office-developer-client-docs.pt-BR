---
title: Propriedade canônica PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356347"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="7b895-103">Propriedade canônica PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="7b895-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="7b895-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b895-105">Contém um valor de campo de título Content-Class [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="7b895-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b895-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="7b895-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="7b895-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7b895-107">None</span></span>  <br/> |
|<span data-ttu-id="7b895-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="7b895-108">Property set:</span></span>  <br/> |<span data-ttu-id="7b895-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="7b895-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="7b895-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="7b895-110">Property name:</span></span>  <br/> |<span data-ttu-id="7b895-111">Content-Class</span><span class="sxs-lookup"><span data-stu-id="7b895-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="7b895-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7b895-112">Data type:</span></span>  <br/> |<span data-ttu-id="7b895-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b895-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b895-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7b895-114">Area:</span></span>  <br/> |<span data-ttu-id="7b895-115">Email</span><span class="sxs-lookup"><span data-stu-id="7b895-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b895-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b895-116">Remarks</span></span>

<span data-ttu-id="7b895-117">Para definir o valor dessa propriedade, os clientes MIME (Multipurpose Internet Message Extensions) devem gravar um campo de título Content-Class com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="7b895-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="7b895-118">Os leitores MIME devem copiar o valor de um campo de título Content-Class para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b895-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7b895-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b895-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b895-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7b895-120">Protocol specifications</span></span>

<span data-ttu-id="7b895-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b895-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b895-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7b895-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b895-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b895-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b895-124">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7b895-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="7b895-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b895-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b895-126">Especifica as propriedades de mensagens codificadas com direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="7b895-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b895-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7b895-127">Header files</span></span>

<span data-ttu-id="7b895-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b895-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b895-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7b895-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b895-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b895-130">See also</span></span>



[<span data-ttu-id="7b895-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7b895-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b895-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7b895-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b895-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7b895-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b895-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7b895-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

