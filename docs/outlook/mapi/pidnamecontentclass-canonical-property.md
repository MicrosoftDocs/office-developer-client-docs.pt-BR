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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384539"
---
# <a name="pidnamecontentclass-canonical-property"></a><span data-ttu-id="e1e05-103">Propriedade canônica PidNameContentClass</span><span class="sxs-lookup"><span data-stu-id="e1e05-103">PidNameContentClass Canonical Property</span></span>

  
  
<span data-ttu-id="e1e05-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1e05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1e05-105">Contém um valor de campo de cabeçalho de classe de conteúdo [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="e1e05-105">Contains an [RFC3282] Content-Class header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1e05-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="e1e05-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="e1e05-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e1e05-107">None</span></span>  <br/> |
|<span data-ttu-id="e1e05-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e1e05-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1e05-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="e1e05-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="e1e05-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="e1e05-110">Property name:</span></span>  <br/> |<span data-ttu-id="e1e05-111">Classe de conteúdo</span><span class="sxs-lookup"><span data-stu-id="e1e05-111">Content-Class</span></span>  <br/> |
|<span data-ttu-id="e1e05-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e1e05-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1e05-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1e05-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e1e05-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e1e05-114">Area:</span></span>  <br/> |<span data-ttu-id="e1e05-115">Email</span><span class="sxs-lookup"><span data-stu-id="e1e05-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1e05-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1e05-116">Remarks</span></span>

<span data-ttu-id="e1e05-117">Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem gravar um campo de cabeçalho de classe de conteúdo com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="e1e05-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write a Content-Class header field with the desired value.</span></span> <span data-ttu-id="e1e05-118">Leitores MIME devem copiar o valor de um campo de cabeçalho de classe de conteúdo para o valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="e1e05-118">MIME readers must copy the value of a Content-Class header field to the value of this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1e05-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1e05-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1e05-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e1e05-120">Protocol specifications</span></span>

<span data-ttu-id="e1e05-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e05-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e05-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1e05-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1e05-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e05-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e05-124">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e1e05-124">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e1e05-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1e05-125">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1e05-126">Especifica as propriedades das mensagens codificadas direitos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="e1e05-126">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1e05-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1e05-127">Header files</span></span>

<span data-ttu-id="e1e05-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1e05-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1e05-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e1e05-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1e05-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1e05-130">See also</span></span>



[<span data-ttu-id="e1e05-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e05-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1e05-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e1e05-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1e05-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e05-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1e05-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e1e05-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

