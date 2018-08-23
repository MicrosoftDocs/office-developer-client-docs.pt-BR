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
ms.openlocfilehash: 91eb93c9cf3afcecef698e27791c06831c13624d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589095"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="45236-103">Propriedade canônica PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="45236-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="45236-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45236-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45236-105">Contém um valor de campo de cabeçalho de conteúdo de [RFC3282]-Base.</span><span class="sxs-lookup"><span data-stu-id="45236-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45236-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="45236-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="45236-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="45236-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="45236-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="45236-108">Property set:</span></span>  <br/> |<span data-ttu-id="45236-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="45236-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="45236-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="45236-110">Property name:</span></span>  <br/> |<span data-ttu-id="45236-111">Base de conteúdo</span><span class="sxs-lookup"><span data-stu-id="45236-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="45236-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="45236-112">Data type:</span></span>  <br/> |<span data-ttu-id="45236-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45236-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="45236-114">Área:</span><span class="sxs-lookup"><span data-stu-id="45236-114">Area:</span></span>  <br/> |<span data-ttu-id="45236-115">Email</span><span class="sxs-lookup"><span data-stu-id="45236-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45236-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="45236-116">Remarks</span></span>

<span data-ttu-id="45236-117">Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem gravar o valor desejado a um campo de cabeçalho de conteúdo-Base em uma entidade MIME que mapeie para o corpo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="45236-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="45236-118">Leitores MIME devem copiar o valor de um campo de cabeçalho de conteúdo-Base em uma entidade MIME tais como o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="45236-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45236-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45236-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45236-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="45236-120">Protocol specifications</span></span>

<span data-ttu-id="45236-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45236-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45236-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="45236-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45236-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45236-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45236-124">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="45236-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45236-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45236-125">Header files</span></span>

<span data-ttu-id="45236-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45236-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="45236-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="45236-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45236-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45236-128">See also</span></span>



[<span data-ttu-id="45236-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45236-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45236-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="45236-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45236-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="45236-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45236-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="45236-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

