---
title: Propriedade canônico de PidLidFileUnder
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: aa0a7f958ed1a5ed4140e87e25bd540123616568
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768464"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="a9411-103">Propriedade canônico de PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="a9411-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="a9411-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a9411-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a9411-105">Especifica o nome sob o qual o contato é arquivado ao exibir uma lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="a9411-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9411-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a9411-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a9411-107">dispidFileUnder</span><span class="sxs-lookup"><span data-stu-id="a9411-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="a9411-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="a9411-108">Property set:</span></span>  <br/> |<span data-ttu-id="a9411-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="a9411-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="a9411-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="a9411-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a9411-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="a9411-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="a9411-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a9411-112">Data type:</span></span>  <br/> |<span data-ttu-id="a9411-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9411-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9411-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a9411-114">Area:</span></span>  <br/> |<span data-ttu-id="a9411-115">Contato</span><span class="sxs-lookup"><span data-stu-id="a9411-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9411-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a9411-116">Remarks</span></span>

<span data-ttu-id="a9411-117">O aplicativo deve tratar essa propriedade como um PT_UNICODE vazia se ele estiver ausente do contato.</span><span class="sxs-lookup"><span data-stu-id="a9411-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a9411-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a9411-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a9411-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a9411-119">Protocol specifications</span></span>

<span data-ttu-id="a9411-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9411-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9411-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a9411-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a9411-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a9411-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a9411-123">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="a9411-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a9411-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9411-124">Header files</span></span>

<span data-ttu-id="a9411-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a9411-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a9411-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a9411-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a9411-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9411-127">See also</span></span>



[<span data-ttu-id="a9411-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a9411-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a9411-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a9411-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a9411-130">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a9411-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a9411-131">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="a9411-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

