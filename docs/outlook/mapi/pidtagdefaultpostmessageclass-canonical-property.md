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
ms.openlocfilehash: 2b4013b311289816f778d7559ee3bcc7dc061538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574332"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a><span data-ttu-id="38995-103">Propriedade canônica PidTagDefaultPostMessageClass</span><span class="sxs-lookup"><span data-stu-id="38995-103">PidTagDefaultPostMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="38995-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38995-105">Contém o nome de uma classe de mensagem do formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="38995-105">Contains the name of a custom form Message class.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38995-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="38995-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38995-107">PR_DEF_POST_MSGCLASS</span><span class="sxs-lookup"><span data-stu-id="38995-107">PR_DEF_POST_MSGCLASS</span></span>  <br/> |
|<span data-ttu-id="38995-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="38995-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38995-109">0x36E5</span><span class="sxs-lookup"><span data-stu-id="38995-109">0x36E5</span></span>  <br/> |
|<span data-ttu-id="38995-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="38995-110">Data type:</span></span>  <br/> |<span data-ttu-id="38995-111">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="38995-111">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="38995-112">Área:</span><span class="sxs-lookup"><span data-stu-id="38995-112">Area:</span></span>  <br/> |<span data-ttu-id="38995-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="38995-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38995-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38995-114">Remarks</span></span>

<span data-ttu-id="38995-115">Se essa propriedade for definida em uma pasta, o valor deve conter exatamente a classe de mensagem de base (por exemplo, "IPM. Contato"para uma pasta de contatos ou"IPM. Compromisso"para uma pasta de calendário), ou começam com a classe de mensagem de base (por exemplo," IPM. Contact.MyContact").</span><span class="sxs-lookup"><span data-stu-id="38995-115">If this property is set on a folder, the value must contain either exactly the base message class (for example, "IPM.Contact" for a contacts folder or "IPM.Appointment" for a calendar folder), or begin with the base message class (for example, "IPM.Contact.MyContact").</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="38995-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="38995-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38995-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="38995-117">Protocol specifications</span></span>

<span data-ttu-id="38995-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38995-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38995-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="38995-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="38995-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38995-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38995-121">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="38995-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38995-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="38995-122">Header files</span></span>

<span data-ttu-id="38995-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38995-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="38995-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="38995-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="38995-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="38995-125">Mapitags.h</span></span>
  
> <span data-ttu-id="38995-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="38995-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38995-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="38995-127">See also</span></span>



[<span data-ttu-id="38995-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="38995-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38995-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="38995-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38995-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="38995-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38995-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="38995-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

