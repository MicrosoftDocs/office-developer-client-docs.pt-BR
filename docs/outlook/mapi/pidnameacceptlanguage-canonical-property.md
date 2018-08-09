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
ms.openlocfilehash: d2c2fb31b722e76034b08077632c817d6adde802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768793"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="839bd-103">Propriedade canônica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="839bd-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="839bd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="839bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="839bd-105">Contém um valor de campo de cabeçalho [RFC3282] Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="839bd-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="839bd-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="839bd-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="839bd-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="839bd-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="839bd-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="839bd-108">Property set:</span></span>  <br/> |<span data-ttu-id="839bd-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="839bd-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="839bd-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="839bd-110">Property name:</span></span>  <br/> |<span data-ttu-id="839bd-111">Idioma aceito</span><span class="sxs-lookup"><span data-stu-id="839bd-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="839bd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="839bd-112">Data type:</span></span>  <br/> |<span data-ttu-id="839bd-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="839bd-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="839bd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="839bd-114">Area:</span></span>  <br/> |<span data-ttu-id="839bd-115">Email</span><span class="sxs-lookup"><span data-stu-id="839bd-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="839bd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="839bd-116">Remarks</span></span>

<span data-ttu-id="839bd-117">Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem escrever um campo de cabeçalho Accept-Language com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="839bd-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="839bd-118">Clientes MIME podem escrever um campo de cabeçalho de idioma aceitar X em vez disso.</span><span class="sxs-lookup"><span data-stu-id="839bd-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="839bd-119">Leitores MIME devem copiar o valor de um campo de cabeçalho para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="839bd-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="839bd-120">Se ambos os campos de cabeçalho estiverem presentes, leitores MIME devem usar o campo de cabeçalho Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="839bd-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="839bd-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="839bd-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="839bd-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="839bd-122">Protocol specifications</span></span>

<span data-ttu-id="839bd-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="839bd-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="839bd-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="839bd-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="839bd-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="839bd-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="839bd-126">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="839bd-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="839bd-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="839bd-127">Header files</span></span>

<span data-ttu-id="839bd-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="839bd-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="839bd-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="839bd-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="839bd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="839bd-130">See also</span></span>



[<span data-ttu-id="839bd-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="839bd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="839bd-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="839bd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="839bd-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="839bd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="839bd-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="839bd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

