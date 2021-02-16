---
title: Propriedade canônica PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331497"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="89633-103">Propriedade canônica PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="89633-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="89633-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89633-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89633-105">Contém um valor de campo de título Content-Base [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="89633-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89633-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="89633-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="89633-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="89633-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="89633-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="89633-108">Property set:</span></span>  <br/> |<span data-ttu-id="89633-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="89633-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="89633-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="89633-110">Property name:</span></span>  <br/> |<span data-ttu-id="89633-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="89633-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="89633-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="89633-112">Data type:</span></span>  <br/> |<span data-ttu-id="89633-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89633-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="89633-114">Área:</span><span class="sxs-lookup"><span data-stu-id="89633-114">Area:</span></span>  <br/> |<span data-ttu-id="89633-115">Email</span><span class="sxs-lookup"><span data-stu-id="89633-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89633-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="89633-116">Remarks</span></span>

<span data-ttu-id="89633-117">Para definir o valor dessa propriedade, os clientes MIME (Multipurpose Internet Message Extensions) devem gravar o valor desejado em um campo de título Content-Base em uma entidade MIME que mapeia para um corpo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="89633-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="89633-118">Os leitores MIME devem copiar o valor de um campo de título Content-Base em tal entidade MIME para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89633-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="89633-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89633-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89633-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="89633-120">Protocol specifications</span></span>

<span data-ttu-id="89633-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89633-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89633-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="89633-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89633-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89633-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89633-124">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="89633-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89633-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="89633-125">Header files</span></span>

<span data-ttu-id="89633-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89633-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="89633-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="89633-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89633-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="89633-128">See also</span></span>



[<span data-ttu-id="89633-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89633-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89633-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="89633-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89633-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="89633-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89633-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="89633-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

