---
title: Propriedade canônica PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342480"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="fea0c-103">Propriedade canônica PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="fea0c-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="fea0c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fea0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fea0c-105">Contém o nome de exibição de um membro da tabela de lista de controle de acesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="fea0c-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fea0c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fea0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fea0c-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="fea0c-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="fea0c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fea0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fea0c-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="fea0c-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="fea0c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fea0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="fea0c-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="fea0c-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="fea0c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fea0c-112">Area:</span></span>  <br/> |<span data-ttu-id="fea0c-113">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="fea0c-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fea0c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fea0c-114">Remarks</span></span>

<span data-ttu-id="fea0c-115">Essas propriedades são usadas pela interface [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) para exibir o nome de um membro de uma tabela ACL, que é uma pessoa ou função com direitos explícitos em uma pasta ou caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="fea0c-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fea0c-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fea0c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fea0c-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="fea0c-117">Protocol specifications</span></span>

<span data-ttu-id="fea0c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fea0c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fea0c-119">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fea0c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fea0c-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fea0c-120">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fea0c-121">Lida com a recuperação de listas de permissões de pastas armazenadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="fea0c-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fea0c-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fea0c-122">Header files</span></span>

<span data-ttu-id="fea0c-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fea0c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fea0c-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fea0c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fea0c-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fea0c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fea0c-126">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="fea0c-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fea0c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fea0c-127">See also</span></span>



[<span data-ttu-id="fea0c-128">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fea0c-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="fea0c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fea0c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fea0c-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fea0c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fea0c-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fea0c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fea0c-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fea0c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

