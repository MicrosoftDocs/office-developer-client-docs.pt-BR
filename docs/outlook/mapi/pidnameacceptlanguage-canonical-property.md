---
title: Propriedade canônica PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 855610c43cfaa64fa69e6987743b137b188d84a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360939"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="281b6-103">Propriedade canônica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="281b6-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="281b6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="281b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="281b6-105">Contém um valor de campo de Accept-Language [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="281b6-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="281b6-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="281b6-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="281b6-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="281b6-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="281b6-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="281b6-108">Property set:</span></span>  <br/> |<span data-ttu-id="281b6-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="281b6-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="281b6-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="281b6-110">Property name:</span></span>  <br/> |<span data-ttu-id="281b6-111">Accept-Language</span><span class="sxs-lookup"><span data-stu-id="281b6-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="281b6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="281b6-112">Data type:</span></span>  <br/> |<span data-ttu-id="281b6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="281b6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="281b6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="281b6-114">Area:</span></span>  <br/> |<span data-ttu-id="281b6-115">Email</span><span class="sxs-lookup"><span data-stu-id="281b6-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="281b6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="281b6-116">Remarks</span></span>

<span data-ttu-id="281b6-117">Para definir o valor dessa propriedade, os clientes MIME (Multipurpose Internet Message Extensions) devem gravar um campo de Accept-Language com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="281b6-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="281b6-118">Em vez disso, os clientes MIME podem escrever um campo de header X-Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="281b6-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="281b6-119">Os leitores MIME devem copiar o valor de qualquer campo de header para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="281b6-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="281b6-120">Se ambos os campos de header estão presentes, os leitores MIME devem usar o campo Accept-Language de Accept-Language de dados.</span><span class="sxs-lookup"><span data-stu-id="281b6-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="281b6-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="281b6-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="281b6-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="281b6-122">Protocol specifications</span></span>

<span data-ttu-id="281b6-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281b6-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281b6-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="281b6-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="281b6-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="281b6-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="281b6-126">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="281b6-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="281b6-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="281b6-127">Header files</span></span>

<span data-ttu-id="281b6-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="281b6-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="281b6-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="281b6-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="281b6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="281b6-130">See also</span></span>



[<span data-ttu-id="281b6-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="281b6-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="281b6-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="281b6-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="281b6-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="281b6-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="281b6-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="281b6-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

