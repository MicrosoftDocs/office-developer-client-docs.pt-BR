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
ms.openlocfilehash: d4e478b053bc1aa81643a60899480ac2ad9d4265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769458"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="8413d-103">Propriedade canônica PidTagMessageClass</span><span class="sxs-lookup"><span data-stu-id="8413d-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="8413d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8413d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8413d-105">Contém uma cadeia de caracteres de texto que identifica a classe de mensagem definidas pelo remetente, como IPM. Nota.</span><span class="sxs-lookup"><span data-stu-id="8413d-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8413d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8413d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8413d-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="8413d-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="8413d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8413d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8413d-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="8413d-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="8413d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8413d-110">Data type:</span></span>  <br/> |<span data-ttu-id="8413d-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="8413d-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="8413d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8413d-112">Area:</span></span>  <br/> |<span data-ttu-id="8413d-113">Comuns</span><span class="sxs-lookup"><span data-stu-id="8413d-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8413d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8413d-114">Remarks</span></span>

<span data-ttu-id="8413d-115">A classe de mensagem especifica o tipo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8413d-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="8413d-116">Determina o conjunto de propriedades definidas para a mensagem, o tipo de informações a mensagem transmite e como lidar com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="8413d-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="8413d-117">Essas propriedades contêm concatenadas com períodos de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8413d-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="8413d-118">Cada cadeia de caracteres representa um nível de subclassificação.</span><span class="sxs-lookup"><span data-stu-id="8413d-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="8413d-119">Por exemplo, IPM. Observação é uma subclasse de IPM e uma superclasse do IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="8413d-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="8413d-120">Essas propriedades devem conter os caracteres ASCII 32 a 127 e não devem terminar com um ponto (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="8413d-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="8413d-121">Operações de classificação e comparação devem tratá-lo como uma cadeia de caracteres diferenciam maiusculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8413d-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="8413d-122">O comprimento máximo de possível é de 255 caracteres, mas, para permitir que a sala MAPI acrescentar o qualificador é recomendável que o comprimento original sejam mantidos em 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8413d-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="8413d-123">Cada mensagem é necessária para fornecer a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8413d-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="8413d-124">Normalmente, o aplicativo cliente criando uma nova mensagem define tão logo [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) retorna com êxito.</span><span class="sxs-lookup"><span data-stu-id="8413d-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="8413d-125">Mas, se a propriedade não tiver sido definida quando o cliente chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md), o armazenamento de mensagens deve defini-la como IPM.</span><span class="sxs-lookup"><span data-stu-id="8413d-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="8413d-126">Os valores definidos pelo MAPI são:</span><span class="sxs-lookup"><span data-stu-id="8413d-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="8413d-127">IPM e CPI servem para ser apenas de superclasse, e uma mensagem deve ter pelo menos um qualificador de subclasse acrescentado antes que estão sendo armazenados ou enviados.</span><span class="sxs-lookup"><span data-stu-id="8413d-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="8413d-128">Para obter mais informações sobre o uso de classe de mensagem, consulte [Classes de mensagens](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8413d-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="8413d-129">Para obter listas de propriedades obrigatórios e opcionais de classes de mensagens, consulte os subtópicos [sobre](message-properties-overview.md)propriedades de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8413d-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="8413d-130">Uma classe de mensagem personalizada pode definir propriedades em um intervalo reservado para uso com essa classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8413d-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="8413d-131">Para obter mais informações, consulte [Sobre identificadores de propriedade](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8413d-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="8413d-132">Controle de classes de mensagem que recebe uma mensagem de entrada da pasta é armazenado em.</span><span class="sxs-lookup"><span data-stu-id="8413d-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="8413d-133">Para obter mais informações, consulte o método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="8413d-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="8413d-134">Para obter mais informações sobre como usar as classes de mensagem com formulários e servidores de formulário, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="8413d-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8413d-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8413d-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8413d-136">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8413d-136">Protocol specifications</span></span>

<span data-ttu-id="8413d-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8413d-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8413d-138">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8413d-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8413d-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8413d-139">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8413d-140">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="8413d-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8413d-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8413d-141">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8413d-142">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8413d-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8413d-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8413d-143">[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8413d-144">Especifica as propriedades e operações que são permitidas para representar mensagens de caixa postal e fax.</span><span class="sxs-lookup"><span data-stu-id="8413d-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8413d-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8413d-145">Header files</span></span>

<span data-ttu-id="8413d-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8413d-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="8413d-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8413d-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="8413d-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8413d-148">Mapitags.h</span></span>
  
> <span data-ttu-id="8413d-149">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8413d-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8413d-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8413d-150">See also</span></span>



[<span data-ttu-id="8413d-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8413d-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8413d-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8413d-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8413d-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8413d-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8413d-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8413d-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

