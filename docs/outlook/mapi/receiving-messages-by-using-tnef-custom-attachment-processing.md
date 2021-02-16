---
title: Recebendo mensagens usando o processamento de anexo personalizado TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429317"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="f71e4-103">Recebendo mensagens usando o processamento de anexo personalizado TNEF</span><span class="sxs-lookup"><span data-stu-id="f71e4-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="f71e4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f71e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f71e4-105">Para receber uma mensagem TNEF com processamento de anexo personalizado:</span><span class="sxs-lookup"><span data-stu-id="f71e4-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="f71e4-106">Importe todas as propriedades transmitíveis — aquelas compatíveis com o sistema de mensagens — da mensagem de entrada para uma nova mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="f71e4-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="f71e4-107">Isso inclui o texto da mensagem, que contém o fluxo de dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="f71e4-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="f71e4-108">Identifique e decodificar o anexo especial que contém o fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="f71e4-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="f71e4-109">Extraia todos os anexos da mensagem de entrada para anexos MAPI na nova mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="f71e4-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="f71e4-110">Os nomes de arquivo recuperados ou outros marcadores de identificação nos anexos devem ser colocados na propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) dos novos anexos para que o método [ITnef::ExtractProps](itnef-extractprops.md) possa associar posteriormente o anexo correto às marcas de anexo codificadas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f71e4-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="f71e4-111">Crie uma interface **IStream** OLE para quebrar o fluxo TNEF decodificado e usar esse objeto juntamente com a nova mensagem MAPI em uma chamada para a [função OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="f71e4-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="f71e4-112">Chame o **método ITnef::ExtractProps** para recuperar as propriedades nãotransmitíveis na mensagem do fluxo de dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="f71e4-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="f71e4-113">Chame o [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) com os sinalizadores MAPI_CREATE e MAPI_MODIFY definidos.</span><span class="sxs-lookup"><span data-stu-id="f71e4-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="f71e4-114">Essa chamada remove as marcas de anexo do texto da mensagem e as converte em informações de posição do anexo na mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="f71e4-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="f71e4-115">Entregar a mensagem por meio do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="f71e4-115">Deliver the message through the MAPI spooler.</span></span>
    

