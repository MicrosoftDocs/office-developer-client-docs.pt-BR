---
title: Propriedade canônica PidTagMemberEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberEntryId
api_type:
- HeaderDef
ms.assetid: b1e166fd-7e15-4371-8510-63001317fb90
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3139f7cc60d19048fb17c64101f279ce377e9b26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769469"
---
# <a name="pidtagmemberentryid-canonical-property"></a><span data-ttu-id="fd215-103">Propriedade canônica PidTagMemberEntryId</span><span class="sxs-lookup"><span data-stu-id="fd215-103">PidTagMemberEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="fd215-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd215-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd215-105">Contém o identificador de entrada de objeto de diretório de um membro de tabela do sistema acesso controle SACL (lista).</span><span class="sxs-lookup"><span data-stu-id="fd215-105">Contains the directory object entry identifier of a system access control list (SACL) table member.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd215-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fd215-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd215-107">PR_MEMBER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fd215-107">PR_MEMBER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="fd215-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fd215-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fd215-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="fd215-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="fd215-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fd215-110">Data type:</span></span>  <br/> |<span data-ttu-id="fd215-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fd215-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fd215-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fd215-112">Area:</span></span>  <br/> |<span data-ttu-id="fd215-113">Regras do lado servidor</span><span class="sxs-lookup"><span data-stu-id="fd215-113">Server Side Rules</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd215-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd215-114">Remarks</span></span>

<span data-ttu-id="fd215-115">Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para identificar exclusivamente uma pessoa ou função aos quais se aplica a SACL.</span><span class="sxs-lookup"><span data-stu-id="fd215-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to uniquely identify a person or role to whom the SACL applies.</span></span> <span data-ttu-id="fd215-116">Depois que o membro é criado na tabela a SACL, **ENTRYID** não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="fd215-116">After a member is created in the SACL table, the **ENTRYID** cannot be changed.</span></span> <span data-ttu-id="fd215-117">Para alterá-lo, você deve excluir o membro de tabela e recriá-la com um diferentes **ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="fd215-117">To change it, you must delete the table member and re-create it with a different **ENTRYID**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd215-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd215-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fd215-119">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fd215-119">Header files</span></span>

<span data-ttu-id="fd215-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd215-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd215-121">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fd215-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="fd215-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fd215-122">Mapitags.h</span></span>
  
> <span data-ttu-id="fd215-123">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fd215-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd215-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd215-124">See also</span></span>



[<span data-ttu-id="fd215-125">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fd215-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd215-126">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fd215-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd215-127">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fd215-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd215-128">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fd215-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

