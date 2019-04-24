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
ms.openlocfilehash: 0329147463db38fb8c547214788366444daed312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319702"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a><span data-ttu-id="7f45f-103">Propriedade canônica PidLidContactCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7f45f-103">PidLidContactCharacterSet Canonical Property</span></span>

  
  
<span data-ttu-id="7f45f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f45f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f45f-105">Especifica o conjunto de caracteres usado para este contato.</span><span class="sxs-lookup"><span data-stu-id="7f45f-105">Specifies the character set used for this contact.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f45f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7f45f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f45f-107">dispidContactCharSet</span><span class="sxs-lookup"><span data-stu-id="7f45f-107">dispidContactCharSet</span></span>  <br/> |
|<span data-ttu-id="7f45f-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="7f45f-108">Property set:</span></span>  <br/> |<span data-ttu-id="7f45f-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="7f45f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="7f45f-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7f45f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7f45f-111">0x00008023</span><span class="sxs-lookup"><span data-stu-id="7f45f-111">0x00008023</span></span>  <br/> |
|<span data-ttu-id="7f45f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7f45f-112">Data type:</span></span>  <br/> |<span data-ttu-id="7f45f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7f45f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7f45f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7f45f-114">Area:</span></span>  <br/> |<span data-ttu-id="7f45f-115">Contato</span><span class="sxs-lookup"><span data-stu-id="7f45f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f45f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f45f-116">Remarks</span></span>

<span data-ttu-id="7f45f-117">Os aplicativos podem usar essa propriedade para ajudar a gerar uma lista de opções dependentes de conjuntos de caracteres para o **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)), **DispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) e \*\*dispidFileUnderId \*\*Propriedades de ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f45f-117">Applications can use this property to aid in generating a character-set dependent list of choices for the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) , **dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) , and **dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) properties.</span></span> <span data-ttu-id="7f45f-118">Se o valor da propriedade for "0x00000000" ou "0x00000001", os aplicativos devem tratar a propriedade como não sendo definida.</span><span class="sxs-lookup"><span data-stu-id="7f45f-118">If the value of the property is "0x00000000" or "0x00000001", applications should treat the property as not being set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f45f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f45f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f45f-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7f45f-120">Protocol specifications</span></span>

<span data-ttu-id="7f45f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f45f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f45f-122">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7f45f-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f45f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f45f-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f45f-124">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="7f45f-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f45f-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7f45f-125">Header files</span></span>

<span data-ttu-id="7f45f-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f45f-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f45f-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7f45f-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f45f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f45f-128">See also</span></span>



[<span data-ttu-id="7f45f-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7f45f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f45f-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7f45f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f45f-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7f45f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f45f-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7f45f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

