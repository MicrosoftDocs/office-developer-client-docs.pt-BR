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
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315453"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a><span data-ttu-id="926b6-103">Propriedade canônica PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="926b6-103">PidLidInternetAccountStamp Canonical Property</span></span>

  
  
<span data-ttu-id="926b6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="926b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="926b6-105">Especifica a ID da conta de email pela qual a mensagem de email é enviada.</span><span class="sxs-lookup"><span data-stu-id="926b6-105">Specifies the email account ID through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="926b6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="926b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="926b6-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="926b6-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="926b6-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="926b6-108">Property set:</span></span>  <br/> |<span data-ttu-id="926b6-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="926b6-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="926b6-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="926b6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="926b6-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="926b6-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="926b6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="926b6-112">Data type:</span></span>  <br/> |<span data-ttu-id="926b6-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="926b6-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="926b6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="926b6-114">Area:</span></span>  <br/> |<span data-ttu-id="926b6-115">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="926b6-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="926b6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="926b6-116">Remarks</span></span>

<span data-ttu-id="926b6-117">O formato dessa cadeia de caracteres depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="926b6-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="926b6-118">Essa propriedade pode ser usada pelo cliente para determinar para qual servidor direcionar o email, mas é opcional e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="926b6-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="926b6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="926b6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="926b6-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="926b6-120">Protocol specifications</span></span>

<span data-ttu-id="926b6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="926b6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="926b6-122">Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="926b6-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="926b6-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="926b6-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="926b6-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="926b6-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="926b6-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="926b6-125">Header files</span></span>

<span data-ttu-id="926b6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="926b6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="926b6-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="926b6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="926b6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="926b6-128">See also</span></span>



[<span data-ttu-id="926b6-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="926b6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="926b6-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="926b6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="926b6-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="926b6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="926b6-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="926b6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

