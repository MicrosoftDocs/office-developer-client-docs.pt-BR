---
title: Propriedade canônica PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357901"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="ff958-103">Propriedade canônica PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="ff958-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="ff958-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff958-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff958-105">Contém o nome de uma classe de mensagem de formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="ff958-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff958-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ff958-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ff958-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="ff958-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="ff958-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ff958-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ff958-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="ff958-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="ff958-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ff958-110">Data type:</span></span>  <br/> |<span data-ttu-id="ff958-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="ff958-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="ff958-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ff958-112">Area:</span></span>  <br/> |<span data-ttu-id="ff958-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="ff958-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff958-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff958-114">Remarks</span></span>

<span data-ttu-id="ff958-115">Se essa propriedade for definida em uma pasta, o valor deverá conter exatamente a classe de mensagem base (por exemplo, "IPM. Contato" para uma pasta de contatos ou "IPM. Compromisso" para uma pasta de calendário) ou comece com a classe de mensagem base (por exemplo, "IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="ff958-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ff958-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff958-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ff958-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ff958-117">Protocol specifications</span></span>

<span data-ttu-id="ff958-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff958-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff958-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ff958-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ff958-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ff958-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ff958-121">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="ff958-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ff958-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ff958-122">Header files</span></span>

<span data-ttu-id="ff958-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ff958-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ff958-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ff958-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ff958-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ff958-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ff958-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ff958-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff958-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff958-127">See also</span></span>



[<span data-ttu-id="ff958-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ff958-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ff958-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ff958-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ff958-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff958-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ff958-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ff958-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

