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
ms.openlocfilehash: f66a570273d78f63ced110a4bdc8a12a49c531b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595241"
---
# <a name="pidnameacceptlanguage-canonical-property"></a><span data-ttu-id="c214b-103">Propriedade canônica PidNameAcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c214b-103">PidNameAcceptLanguage Canonical Property</span></span>

  
  
<span data-ttu-id="c214b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c214b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c214b-105">Contém um valor de campo de cabeçalho [RFC3282] Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="c214b-105">Contains an [RFC3282] Accept-Language header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c214b-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="c214b-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="c214b-107">AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c214b-107">AcceptLanguage</span></span>  <br/> |
|<span data-ttu-id="c214b-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="c214b-108">Property set:</span></span>  <br/> |<span data-ttu-id="c214b-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="c214b-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="c214b-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="c214b-110">Property name:</span></span>  <br/> |<span data-ttu-id="c214b-111">Idioma aceito</span><span class="sxs-lookup"><span data-stu-id="c214b-111">Accept-Language</span></span>  <br/> |
|<span data-ttu-id="c214b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c214b-112">Data type:</span></span>  <br/> |<span data-ttu-id="c214b-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c214b-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c214b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c214b-114">Area:</span></span>  <br/> |<span data-ttu-id="c214b-115">Email</span><span class="sxs-lookup"><span data-stu-id="c214b-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c214b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c214b-116">Remarks</span></span>

<span data-ttu-id="c214b-117">Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem escrever um campo de cabeçalho Accept-Language com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="c214b-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients should write an Accept-Language header field with the desired value.</span></span> <span data-ttu-id="c214b-118">Clientes MIME podem escrever um campo de cabeçalho de idioma aceitar X em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c214b-118">MIME clients may write an X-Accept-Language header field instead.</span></span> <span data-ttu-id="c214b-119">Leitores MIME devem copiar o valor de um campo de cabeçalho para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c214b-119">MIME readers should copy the value of either header field to the value of this property.</span></span> <span data-ttu-id="c214b-120">Se ambos os campos de cabeçalho estiverem presentes, leitores MIME devem usar o campo de cabeçalho Accept-Language.</span><span class="sxs-lookup"><span data-stu-id="c214b-120">If both header fields are present, MIME readers should use the Accept-Language header field.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c214b-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c214b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c214b-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c214b-122">Protocol specifications</span></span>

<span data-ttu-id="c214b-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c214b-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c214b-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c214b-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c214b-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c214b-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c214b-126">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c214b-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c214b-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c214b-127">Header files</span></span>

<span data-ttu-id="c214b-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c214b-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="c214b-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c214b-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c214b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c214b-130">See also</span></span>



[<span data-ttu-id="c214b-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c214b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c214b-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c214b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c214b-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c214b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c214b-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c214b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

