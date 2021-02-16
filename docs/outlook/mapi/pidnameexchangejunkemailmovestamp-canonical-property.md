---
title: Propriedade canônica PidNameExchangeJunkEmailMoveStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540942"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="70fd0-103">Propriedade canônica PidNameExchangeJunkEmailMoveStamp</span><span class="sxs-lookup"><span data-stu-id="70fd0-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="70fd0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70fd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70fd0-105">Contém o valor da mensagem persistente que indica que a mensagem não deve ser processada por um filtro de spam porque ela já foi processada ou está segura.</span><span class="sxs-lookup"><span data-stu-id="70fd0-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70fd0-106">Nomes amigáveis:</span><span class="sxs-lookup"><span data-stu-id="70fd0-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="70fd0-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="70fd0-107">None</span></span>  <br/> |
|<span data-ttu-id="70fd0-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="70fd0-108">Property set:</span></span>  <br/> |<span data-ttu-id="70fd0-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="70fd0-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="70fd0-110">Nome da propriedade:</span><span class="sxs-lookup"><span data-stu-id="70fd0-110">Property name:</span></span>  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="70fd0-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="70fd0-111">Data type:</span></span>  <br/> |<span data-ttu-id="70fd0-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="70fd0-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="70fd0-113">Área:</span><span class="sxs-lookup"><span data-stu-id="70fd0-113">Area:</span></span>  <br/> |<span data-ttu-id="70fd0-114">Mensagens seguras</span><span class="sxs-lookup"><span data-stu-id="70fd0-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70fd0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="70fd0-115">Remarks</span></span>

<span data-ttu-id="70fd0-116">Essa propriedade é carimbada em todas as mensagens movidas pela Regra de Lixo Eletrônico ou que, de outra forma, é um conteúdo confiável.</span><span class="sxs-lookup"><span data-stu-id="70fd0-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70fd0-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="70fd0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70fd0-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="70fd0-118">Protocol specifications</span></span>

<span data-ttu-id="70fd0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70fd0-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70fd0-120">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="70fd0-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70fd0-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70fd0-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70fd0-122">Permite a manipulação de listas de bloqueio/autorização e a determinação de mensagens de lixo eletrônico.</span><span class="sxs-lookup"><span data-stu-id="70fd0-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="70fd0-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70fd0-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70fd0-124">Especifica as propriedades e operações que representam itens RSS.</span><span class="sxs-lookup"><span data-stu-id="70fd0-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70fd0-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="70fd0-125">Header files</span></span>

<span data-ttu-id="70fd0-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70fd0-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="70fd0-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="70fd0-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70fd0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="70fd0-128">See also</span></span>



[<span data-ttu-id="70fd0-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="70fd0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70fd0-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="70fd0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70fd0-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="70fd0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70fd0-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="70fd0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

