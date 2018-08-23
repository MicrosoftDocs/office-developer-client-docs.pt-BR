---
title: Propriedade canônica PidLidFileUnder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 58037aa74cbccb67ebd480650fd0ae967a12cbf3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575690"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="dd35c-103">Propriedade canônica PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="dd35c-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="dd35c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd35c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd35c-105">Especifica o nome sob o qual o contato é arquivado ao exibir uma lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="dd35c-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dd35c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dd35c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dd35c-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="dd35c-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="dd35c-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="dd35c-108">Property set:</span></span>  <br/> |<span data-ttu-id="dd35c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="dd35c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="dd35c-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="dd35c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dd35c-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="dd35c-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="dd35c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dd35c-112">Data type:</span></span>  <br/> |<span data-ttu-id="dd35c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dd35c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="dd35c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="dd35c-114">Area:</span></span>  <br/> |<span data-ttu-id="dd35c-115">Contato</span><span class="sxs-lookup"><span data-stu-id="dd35c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd35c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd35c-116">Remarks</span></span>

<span data-ttu-id="dd35c-117">O aplicativo deve tratar essa propriedade como um PT_UNICODE vazia se ele estiver ausente do contato.</span><span class="sxs-lookup"><span data-stu-id="dd35c-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dd35c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd35c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dd35c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dd35c-119">Protocol specifications</span></span>

<span data-ttu-id="dd35c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd35c-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd35c-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="dd35c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dd35c-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dd35c-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dd35c-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="dd35c-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dd35c-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dd35c-124">Header files</span></span>

<span data-ttu-id="dd35c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dd35c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dd35c-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dd35c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dd35c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd35c-127">See also</span></span>



[<span data-ttu-id="dd35c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dd35c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dd35c-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="dd35c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dd35c-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dd35c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dd35c-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dd35c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

