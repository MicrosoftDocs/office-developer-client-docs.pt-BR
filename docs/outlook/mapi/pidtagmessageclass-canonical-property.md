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
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="8b7ae-103">Propriedade canônica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="8b7ae-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="8b7ae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b7ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b7ae-105">Contém uma cadeia de caracteres de texto que identifica a classe de mensagem definida pelo remetente, como IPM. Observação.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b7ae-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8b7ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b7ae-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="8b7ae-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="8b7ae-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8b7ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b7ae-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="8b7ae-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="8b7ae-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8b7ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b7ae-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8b7ae-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8b7ae-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8b7ae-112">Area:</span></span>  <br/> |<span data-ttu-id="8b7ae-113">Comum</span><span class="sxs-lookup"><span data-stu-id="8b7ae-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b7ae-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b7ae-114">Remarks</span></span>

<span data-ttu-id="8b7ae-115">A classe de mensagem Especifica o tipo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="8b7ae-116">Ele determina o conjunto de propriedades definido para a mensagem, o tipo de informação que a mensagem transmite e como lidar com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="8b7ae-117">Essas propriedades contêm cadeias de caracteres concatenadas com pontos.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="8b7ae-118">Cada cadeia de caracteres representa um nível de subclassificação.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="8b7ae-119">Por exemplo, IPM. Observe que é uma subclasse de IPM e uma superclasse de IPM. Note. Private.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="8b7ae-120">Essas propriedades devem consistir nos caracteres ASCII 32 a 127 e não devem terminar com um ponto (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="8b7ae-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="8b7ae-121">As operações de classificação e comparação devem tratá-lo como uma cadeia de caracteres que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="8b7ae-122">O tamanho máximo possível é de 255 caracteres, mas para permitir que a sala de MAPI Anexe os qualificadores, é recomendável que o comprimento original seja mantido abaixo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="8b7ae-123">Todas as mensagens são necessárias para fornecer essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="8b7ae-124">Normalmente, o aplicativo cliente que cria uma nova mensagem a define assim que [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) é retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="8b7ae-125">Mas, se a propriedade não tiver sido definida quando o cliente chama [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), o repositório de mensagens deverá defini-la como IPM.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="8b7ae-126">Os valores definidos por MAPI são:</span><span class="sxs-lookup"><span data-stu-id="8b7ae-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="8b7ae-127">IPM e IPC se destinam apenas a superclasses e uma mensagem deve ter pelo menos um qualificador de subclasse acrescentado antes de ser armazenado ou enviado.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="8b7ae-128">Para obter mais informações sobre o uso da classe de mensagem, consulte [Message classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ae-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="8b7ae-129">Para obter listas de propriedades obrigatórias e opcionais para classes de mensagens, consulte os subtópicos [sobre propriedades de mensagem](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ae-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="8b7ae-130">Uma classe de mensagem personalizada pode definir propriedades em um intervalo reservado para uso somente com essa classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="8b7ae-131">Para obter mais informações, consulte [about Property Identifiers](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ae-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="8b7ae-132">Classes de mensagens controle em qual pasta de recebimento uma mensagem de entrada é armazenada.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="8b7ae-133">Para obter mais informações, consulte o método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="8b7ae-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="8b7ae-134">Para obter mais informações sobre como usar classes de mensagem com formulários e servidores de formulário, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="8b7ae-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b7ae-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b7ae-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b7ae-136">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="8b7ae-136">Protocol specifications</span></span>

<span data-ttu-id="8b7ae-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b7ae-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b7ae-138">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b7ae-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b7ae-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b7ae-140">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8b7ae-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b7ae-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b7ae-142">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8b7ae-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b7ae-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b7ae-144">Especifica as propriedades e as operações que são permitidas para representar a caixa postal e mensagens de fax.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b7ae-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b7ae-145">Header files</span></span>

<span data-ttu-id="8b7ae-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b7ae-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b7ae-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b7ae-148">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8b7ae-148">Mapitags.h</span></span>
  
> <span data-ttu-id="8b7ae-149">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8b7ae-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b7ae-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b7ae-150">See also</span></span>



[<span data-ttu-id="8b7ae-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7ae-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b7ae-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7ae-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b7ae-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7ae-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b7ae-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8b7ae-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

