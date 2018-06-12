---
title: Propriedade canônico de PidTagMemberName
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 694cc4e4626fb9070927232bb72252f716eb458e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769453"
---
# <a name="pidtagmembername-canonical-property"></a><span data-ttu-id="a31cb-103">Propriedade canônico de PidTagMemberName</span><span class="sxs-lookup"><span data-stu-id="a31cb-103">PidTagMemberName Canonical Property</span></span>

  
  
<span data-ttu-id="a31cb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a31cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a31cb-105">Contém o nome de exibição de um membro da tabela de lista (ACL) do controle do access.</span><span class="sxs-lookup"><span data-stu-id="a31cb-105">Contains the display name of a member of the access control list (ACL) table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a31cb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a31cb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a31cb-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a31cb-107">PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a31cb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a31cb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a31cb-109">0x6672</span><span class="sxs-lookup"><span data-stu-id="a31cb-109">0x6672</span></span>  <br/> |
|<span data-ttu-id="a31cb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a31cb-110">Data type:</span></span>  <br/> |<span data-ttu-id="a31cb-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a31cb-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a31cb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a31cb-112">Area:</span></span>  <br/> |<span data-ttu-id="a31cb-113">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="a31cb-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a31cb-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a31cb-114">Remarks</span></span>

<span data-ttu-id="a31cb-115">Essas propriedades são usadas pelo [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interface para exibir o nome de um membro de uma tabela ACL, que é uma pessoa ou função com direitos explícitos em uma pasta ou caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a31cb-115">These properties are used by the [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface to display the name of a member of an ACL table, which is a person or role with explicit rights on a folder or mailbox.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a31cb-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a31cb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a31cb-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a31cb-117">Protocol specifications</span></span>

<span data-ttu-id="a31cb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a31cb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a31cb-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a31cb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a31cb-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a31cb-120">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a31cb-121">Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.</span><span class="sxs-lookup"><span data-stu-id="a31cb-121">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a31cb-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a31cb-122">Header files</span></span>

<span data-ttu-id="a31cb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a31cb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a31cb-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a31cb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a31cb-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a31cb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a31cb-126">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="a31cb-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a31cb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a31cb-127">See also</span></span>



[<span data-ttu-id="a31cb-128">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a31cb-128">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="a31cb-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a31cb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a31cb-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a31cb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a31cb-131">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a31cb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a31cb-132">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="a31cb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

