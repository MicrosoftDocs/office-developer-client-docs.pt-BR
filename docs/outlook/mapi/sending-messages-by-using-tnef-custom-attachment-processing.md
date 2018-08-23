---
title: Enviar mensagens usando o processamento de anexos personalizado com TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 0c7cdf754b2a4b38516b1ac06074fdba9d2227f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577741"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="dc5ab-103">Enviar mensagens usando o processamento de anexos personalizado com TNEF</span><span class="sxs-lookup"><span data-stu-id="dc5ab-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="dc5ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc5ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc5ab-105">Para personalizar o processamento de anexo ao enviar uma mensagem:</span><span class="sxs-lookup"><span data-stu-id="dc5ab-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="dc5ab-106">Obter um objeto TNEF passando uma interface **IStream** e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5ab-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="dc5ab-107">Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5ab-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="dc5ab-108">Use métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades suportadas pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="dc5ab-109">Em um horário adequado grave essas propriedades para o sistema de mensagens no formato exigido pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="dc5ab-110">Chame o método [ITnef::AddProps](itnef-addprops.md) para adicionar apenas as propriedades da mensagem — ou seja, nenhuma das propriedades nos anexos —, definindo o sinalizador TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="dc5ab-111">Chamar [ITnef::AddProps](itnef-addprops.md) com estes itens: o sinalizador TNEF_PROP_EXCLUDE, uma matriz de marca de propriedade que contém o **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) propriedade e um identificador de anexo que especifica o anexo a ser processado.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="dc5ab-112">Use o método [ITnef::SetProps](itnef-setprops.md) para adicionar a marca de propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) com uma cadeia de caracteres exclusiva que identifica o anexo a sistema de mensagens, se o anexo tiver um nome de arquivo que o não oferece suporte ao sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="dc5ab-113">Por exemplo, vários anexos com o mesmo nome de arquivo original ou um nome de arquivo que não é um nome de arquivo válido para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="dc5ab-114">Esta cadeia de caracteres será ser usada com um número de chave ao escrever as marcas de anexo no texto da mensagem marcados para associar um anexo com seus dados.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="dc5ab-115">Para obter mais informações, consulte, [TNEF-Tagged o texto da mensagem](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="dc5ab-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="dc5ab-116">Repita as chamadas **AddProps** e **SetProps** para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="dc5ab-117">Chame o método [ITnef::Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF depois que todas as propriedades solicitadas são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="dc5ab-118">Obter o texto da mensagem marcados chamando o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5ab-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="dc5ab-119">Esse texto marcado é lido usando os métodos da interface **IStream** , codificados usando o modelo de anexo do sistema de mensagens e gravado em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="dc5ab-120">Chame o método [IUnknown:: Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto [ITnef](itnefiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="dc5ab-120">Call the [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="dc5ab-121">Escreva os anexos restantes para o sistema de mensagens por meio do modelo de anexo do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="dc5ab-122">Seu provedor de transporte deve usar o procedimento descrito anteriormente para o processo de anexos.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="dc5ab-123">Se não for possível, o provedor de transporte deve usar as seguintes etapas para processamento de anexo personalizada:</span><span class="sxs-lookup"><span data-stu-id="dc5ab-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="dc5ab-124">O provedor de transporte garante que as propriedades **PR_ATTACH_TRANSPORT_NAME** de todos os anexos contenham valores exclusivos que são identificadores de anexo válido para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="dc5ab-125">O provedor de transporte, em seguida, usa uma única chamada de **ITnef::AddProps** para cada anexo, passando o sinalizador TNEF_PROP_CONTAINED.</span><span class="sxs-lookup"><span data-stu-id="dc5ab-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

