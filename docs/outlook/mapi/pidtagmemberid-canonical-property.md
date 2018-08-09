---
title: Propriedade canônica PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce6925f40e09261494e4edbcbd7314728debbe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769477"
---
# <a name="pidtagmemberid-canonical-property"></a><span data-ttu-id="81390-103">Propriedade canônica PidTagMemberId</span><span class="sxs-lookup"><span data-stu-id="81390-103">PidTagMemberId Canonical Property</span></span>

  
  
<span data-ttu-id="81390-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81390-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81390-105">Contém o identificador de um membro de tabela que tenha os direitos descritos em uma pasta do Microsoft Exchange Server ou a caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="81390-105">Contains the identifier of a table member that has the described rights on a Microsoft Exchange Server folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81390-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="81390-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81390-107">PR_MEMBER_ID</span><span class="sxs-lookup"><span data-stu-id="81390-107">PR_MEMBER_ID</span></span>  <br/> |
|<span data-ttu-id="81390-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81390-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81390-109">0x6671</span><span class="sxs-lookup"><span data-stu-id="81390-109">0x6671</span></span>  <br/> |
|<span data-ttu-id="81390-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="81390-110">Data type:</span></span>  <br/> |<span data-ttu-id="81390-111">PT_I8</span><span class="sxs-lookup"><span data-stu-id="81390-111">PT_I8</span></span>  <br/> |
|<span data-ttu-id="81390-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81390-112">Area:</span></span>  <br/> |<span data-ttu-id="81390-113">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="81390-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81390-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81390-114">Remarks</span></span>

<span data-ttu-id="81390-115">Esta propriedade retorna um identificador exclusivo para a tabela.</span><span class="sxs-lookup"><span data-stu-id="81390-115">This property returns an identifier unique to the table.</span></span> <span data-ttu-id="81390-116">Um identificador de usuário do diretório é associado a cada identificador de membro e é fornecido por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="81390-116">A directory user identifier is associated with each member identifier and is given by this property.</span></span> <span data-ttu-id="81390-117">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para recuperar o identificador de entrada de diretório do membro com direitos explícitos em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="81390-117">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to retrieve the directory entry identifier of a member with explicit rights on a folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81390-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81390-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81390-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="81390-119">Protocol specifications</span></span>

<span data-ttu-id="81390-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81390-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81390-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="81390-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81390-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81390-122">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81390-123">Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.</span><span class="sxs-lookup"><span data-stu-id="81390-123">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81390-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81390-124">Header files</span></span>

<span data-ttu-id="81390-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81390-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="81390-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="81390-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="81390-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81390-127">Mapitags.h</span></span>
  
> <span data-ttu-id="81390-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="81390-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81390-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="81390-129">See also</span></span>



[<span data-ttu-id="81390-130">Propriedade canônica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="81390-130">PidTagMemberEntryId Canonical Property</span></span>](pidtagmemberentryid-canonical-property.md)


[<span data-ttu-id="81390-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81390-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81390-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="81390-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81390-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="81390-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81390-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="81390-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

