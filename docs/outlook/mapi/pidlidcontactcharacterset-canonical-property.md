---
title: Propriedade canônica PidLidContactCharacterSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9706d1060347609708070140aae51d9dcadbb9c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768368"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="4da9a-103">Propriedade canônica PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4da9a-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="4da9a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4da9a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4da9a-105">Especifica o conjunto de caracteres usado para esse contato.</span><span class="sxs-lookup"><span data-stu-id="4da9a-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4da9a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4da9a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4da9a-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="4da9a-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="4da9a-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4da9a-108">Property set:</span></span>  <br/> |<span data-ttu-id="4da9a-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="4da9a-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="4da9a-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4da9a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4da9a-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="4da9a-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="4da9a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4da9a-112">Data type:</span></span>  <br/> |<span data-ttu-id="4da9a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4da9a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4da9a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4da9a-114">Area:</span></span>  <br/> |<span data-ttu-id="4da9a-115">Contato</span><span class="sxs-lookup"><span data-stu-id="4da9a-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4da9a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4da9a-116">Remarks</span></span>

<span data-ttu-id="4da9a-117">Aplicativos podem usar essa propriedade para auxiliar no gerando uma lista de dependente de conjunto de caracteres de opções para o **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) e **dispidFileUnderId **Propriedades ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="4da9a-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="4da9a-118">Se o valor da propriedade é "0x00000000" ou "0x00000001", os aplicativos devem tratar a propriedade como não sendo definido.</span><span class="sxs-lookup"><span data-stu-id="4da9a-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4da9a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4da9a-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4da9a-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4da9a-120">Protocol specifications</span></span>

<span data-ttu-id="4da9a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da9a-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da9a-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4da9a-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4da9a-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4da9a-123">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4da9a-124">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4da9a-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4da9a-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4da9a-125">Header files</span></span>

<span data-ttu-id="4da9a-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4da9a-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4da9a-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4da9a-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4da9a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4da9a-128">See also</span></span>



[<span data-ttu-id="4da9a-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4da9a-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4da9a-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4da9a-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4da9a-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4da9a-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4da9a-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4da9a-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

