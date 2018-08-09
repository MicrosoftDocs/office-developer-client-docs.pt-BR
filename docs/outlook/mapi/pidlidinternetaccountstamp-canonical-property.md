---
title: Propriedade canônica PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 49732f30461e05e83c130f9cc24129cc86baa75f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768505"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="10e19-103">Propriedade canônica PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="10e19-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="10e19-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10e19-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10e19-105">Especifica a ID da conta de email através do qual a mensagem de email é enviada.</span><span class="sxs-lookup"><span data-stu-id="10e19-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10e19-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="10e19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10e19-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="10e19-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="10e19-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="10e19-108">Property set:</span></span>  <br/> |<span data-ttu-id="10e19-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="10e19-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="10e19-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="10e19-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10e19-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="10e19-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="10e19-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="10e19-112">Data type:</span></span>  <br/> |<span data-ttu-id="10e19-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10e19-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10e19-114">Área:</span><span class="sxs-lookup"><span data-stu-id="10e19-114">Area:</span></span>  <br/> |<span data-ttu-id="10e19-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="10e19-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10e19-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10e19-116">Remarks</span></span>

<span data-ttu-id="10e19-117">O formato dessa cadeia de caracteres é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="10e19-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="10e19-118">Essa propriedade pode ser usada pelo cliente para determinar em qual servidor para direcionar o email para, mas é opcional e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="10e19-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10e19-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="10e19-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10e19-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="10e19-120">Protocol specifications</span></span>

<span data-ttu-id="10e19-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10e19-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10e19-122">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="10e19-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10e19-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10e19-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10e19-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="10e19-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10e19-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10e19-125">Header files</span></span>

<span data-ttu-id="10e19-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10e19-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="10e19-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="10e19-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10e19-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="10e19-128">See also</span></span>



[<span data-ttu-id="10e19-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="10e19-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10e19-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="10e19-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10e19-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="10e19-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10e19-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="10e19-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
