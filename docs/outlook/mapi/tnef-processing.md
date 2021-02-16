---
title: Processamento TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339596"
---
# <a name="tnef-processing"></a><span data-ttu-id="2be0e-103">Processamento TNEF</span><span class="sxs-lookup"><span data-stu-id="2be0e-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="2be0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2be0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2be0e-105">A série de ações a seguir descreve como os transporte usam métodos TNEF para processar mensagens de saída e de entrada.</span><span class="sxs-lookup"><span data-stu-id="2be0e-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="2be0e-106">**Para enviar uma mensagem que inclui um fluxo TNEF**</span><span class="sxs-lookup"><span data-stu-id="2be0e-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="2be0e-107">Processe as propriedades de mensagem que são suportadas pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2be0e-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="2be0e-108">Marque a mensagem de uma maneira específica de implementação para que o provedor de transporte de recebimento possa determinar que a mensagem requer processamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="2be0e-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="2be0e-109">Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagens SMTP pode adicionar um campo de header personalizado como "X-CONTAINS-TNEF" para indicar que a mensagem contém dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="2be0e-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="2be0e-110">Obtenha um objeto TNEF e use-o para encapsular as propriedades de mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="2be0e-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="2be0e-111">Codificar o fluxo TNEF usando o modelo de anexo do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2be0e-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="2be0e-112">Por exemplo, se o modelo de anexo subjacente for para codificar anexos e aendá-los ao texto da mensagem, o provedor de transporte deverá codificar o fluxo TNEF em outro anexo.</span><span class="sxs-lookup"><span data-stu-id="2be0e-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="2be0e-113">O provedor de transporte também deve implementar um método para reconhecer qual anexo contém o fluxo TNEF codificado quando recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2be0e-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="2be0e-114">A maneira padrão de marcar esse anexo é dar a ele um nome de arquivo de anexo "WINMAIL. DAT".</span><span class="sxs-lookup"><span data-stu-id="2be0e-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="2be0e-115">Se o provedor de transporte fizer isso, qualquer outro provedor de transporte habilitado para TNEF que seguir essa convenção poderá interoperar com ela.</span><span class="sxs-lookup"><span data-stu-id="2be0e-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="2be0e-116">Use [ITnef : métodos](itnefiunknown.md) de interface IUnknown para inserir marcas que descrevem as posições dos anexos de mensagem no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2be0e-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="2be0e-117">Acesse o texto da mensagem marcado por [meio dos métodos IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e envie-o para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2be0e-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="2be0e-118">**Para recuperar propriedades encapsuladas**</span><span class="sxs-lookup"><span data-stu-id="2be0e-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="2be0e-119">Escreva as propriedades suportadas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem marcado que contém as propriedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="2be0e-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="2be0e-120">Decodificar o fluxo TNEF do anexo apropriado.</span><span class="sxs-lookup"><span data-stu-id="2be0e-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="2be0e-121">Decodificar quaisquer outros anexos e gravar em novos anexos MAPI em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2be0e-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="2be0e-122">Abra o fluxo TNEF para decodificação usando a [função OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="2be0e-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="2be0e-123">Use o [método ITnef::ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="2be0e-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="2be0e-124">Quaisquer propriedades codificadas que sejam duplicatas de propriedades não codificadas substituirão as propriedades não codificadas quando as propriedades codificadas são decodificadas.</span><span class="sxs-lookup"><span data-stu-id="2be0e-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="2be0e-125">Use o [método ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar posições de anexo das marcas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="2be0e-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

