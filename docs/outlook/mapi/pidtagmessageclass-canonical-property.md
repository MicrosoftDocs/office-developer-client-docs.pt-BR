---
title: Propriedade canônica PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359259"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="77fff-103">Propriedade canônica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="77fff-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="77fff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77fff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77fff-105">Contém uma cadeia de texto que identifica a classe de mensagem definida pelo remetente, como IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="77fff-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77fff-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="77fff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="77fff-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="77fff-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="77fff-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="77fff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="77fff-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="77fff-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="77fff-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="77fff-110">Data type:</span></span>  <br/> |<span data-ttu-id="77fff-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="77fff-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="77fff-112">Área:</span><span class="sxs-lookup"><span data-stu-id="77fff-112">Area:</span></span>  <br/> |<span data-ttu-id="77fff-113">Comum</span><span class="sxs-lookup"><span data-stu-id="77fff-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77fff-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="77fff-114">Remarks</span></span>

<span data-ttu-id="77fff-115">A classe de mensagem especifica o tipo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="77fff-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="77fff-116">Ele determina o conjunto de propriedades definidas para a mensagem, o tipo de informação que a mensagem transmite e como lidar com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="77fff-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="77fff-117">Essas propriedades contêm cadeias de caracteres concatenadas com períodos.</span><span class="sxs-lookup"><span data-stu-id="77fff-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="77fff-118">Cada cadeia de caracteres representa um nível de subclasse.</span><span class="sxs-lookup"><span data-stu-id="77fff-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="77fff-119">Por exemplo, IPM. Observação é uma subclasse do IPM e uma superclasse do IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="77fff-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="77fff-120">Essas propriedades devem consistir nos caracteres ASCII de 32 a 127 e não terminar com um ponto (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="77fff-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="77fff-121">As operações de classificação e comparação devem tratá-la como uma cadeia de caracteres que não faz maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="77fff-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="77fff-122">O comprimento máximo possível é de 255 caracteres, mas para permitir que a sala MAPI a append qualificadores, é recomendável que o comprimento original seja mantido abaixo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="77fff-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="77fff-123">Cada mensagem é necessária para fornecer essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="77fff-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="77fff-124">Normalmente, o aplicativo cliente que cria uma nova mensagem a define assim que [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) retorna com êxito.</span><span class="sxs-lookup"><span data-stu-id="77fff-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="77fff-125">Mas se a propriedade não tiver sido definida quando o cliente chamar [IMAPIProp::SaveChanges,](imapiprop-savechanges.md)o armazenamento de mensagens deverá defini-la como IPM.</span><span class="sxs-lookup"><span data-stu-id="77fff-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="77fff-126">Os valores definidos por MAPI são:</span><span class="sxs-lookup"><span data-stu-id="77fff-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="77fff-127">IPM e IPC destinam-se a ser apenas superclasses, e uma mensagem deve ter pelo menos um qualificador de subclasse anexado antes de ser armazenado ou enviado.</span><span class="sxs-lookup"><span data-stu-id="77fff-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="77fff-128">Para obter mais informações sobre o uso da classe de mensagens, consulte [Classes de mensagem.](mapi-message-classes.md)</span><span class="sxs-lookup"><span data-stu-id="77fff-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="77fff-129">Para listas de propriedades opcionais e obrigatórios para classes de mensagens, consulte os subtópicos sobre propriedades [de mensagem.](message-properties-overview.md)</span><span class="sxs-lookup"><span data-stu-id="77fff-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="77fff-130">Uma classe de mensagem personalizada pode definir propriedades em um intervalo reservado para uso somente com essa classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="77fff-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="77fff-131">Para obter mais informações, consulte [Sobre identificadores de propriedade.](mapi-property-identifier-overview.md)</span><span class="sxs-lookup"><span data-stu-id="77fff-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="77fff-132">Classes de mensagem controlam em qual pasta de recebimento uma mensagem de entrada é armazenada.</span><span class="sxs-lookup"><span data-stu-id="77fff-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="77fff-133">Para obter mais informações, consulte o [método IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="77fff-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="77fff-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="77fff-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="77fff-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="77fff-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="77fff-136">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="77fff-136">Protocol specifications</span></span>

<span data-ttu-id="77fff-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77fff-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77fff-138">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="77fff-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="77fff-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77fff-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77fff-140">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="77fff-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="77fff-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77fff-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77fff-142">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="77fff-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="77fff-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77fff-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="77fff-144">Especifica as propriedades e operações permitidas para representar mensagens de caixa postal e fax.</span><span class="sxs-lookup"><span data-stu-id="77fff-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="77fff-145">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="77fff-145">Header files</span></span>

<span data-ttu-id="77fff-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77fff-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="77fff-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="77fff-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="77fff-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="77fff-148">Mapitags.h</span></span>
  
> <span data-ttu-id="77fff-149">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="77fff-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="77fff-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="77fff-150">See also</span></span>



[<span data-ttu-id="77fff-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="77fff-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="77fff-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="77fff-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="77fff-153">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="77fff-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="77fff-154">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="77fff-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

