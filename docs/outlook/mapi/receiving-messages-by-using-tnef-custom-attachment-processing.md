---
title: Receber mensagens usando o processamento de anexos personalizado com TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 18fc0983554284355dcdfb301fd41a0161a860fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770236"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="e7d31-103">Receber mensagens usando o processamento de anexos personalizado com TNEF</span><span class="sxs-lookup"><span data-stu-id="e7d31-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="e7d31-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7d31-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7d31-105">Para receber uma mensagem TNEF com processamento de anexo personalizada:</span><span class="sxs-lookup"><span data-stu-id="e7d31-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="e7d31-106">Importar todas as propriedades transmittable — aqueles que suporta o sistema de mensagens — da mensagem de entrada em uma nova mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7d31-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="e7d31-107">Isso inclui o texto da mensagem, que contém o fluxo de dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="e7d31-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="e7d31-108">Identifique e decodificar o anexo especial que contém o fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="e7d31-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="e7d31-109">Extraia todos os anexos da mensagem de entrada em anexos de MAPI sobre a nova mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7d31-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="e7d31-110">Os nomes de arquivo recuperado ou outro marcadores de identificação sobre os anexos, devem ser colocado na propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) os anexos de novo assim que o método [ITnef::ExtractProps](itnef-extractprops.md) mais tarde pode associar o anexo correto com as marcas de anexo codificadas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7d31-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="e7d31-111">Crie uma interface **IStream** do OLE para quebrar em torno do fluxo TNEF decodificado e usar esse objeto, juntamente com a nova mensagem MAPI em uma chamada para a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d31-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="e7d31-112">Chame o método **ITnef::ExtractProps** para recuperar as propriedades de nontransmittable na mensagem de fluxo de dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="e7d31-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="e7d31-113">Chame o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) com o conjunto de sinalizadores MAPI_CREATE e MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="e7d31-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="e7d31-114">Essa chamada remove as marcas de anexo do texto da mensagem e converte-os em informações de posição de anexo na mensagem de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7d31-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="e7d31-115">Entrega a mensagem por meio do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e7d31-115">Deliver the message through the MAPI spooler.</span></span>
    

