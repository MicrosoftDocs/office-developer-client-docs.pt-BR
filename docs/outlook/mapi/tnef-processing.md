---
title: Processamento TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399564"
---
# <a name="tnef-processing"></a><span data-ttu-id="7bc78-103">Processamento TNEF</span><span class="sxs-lookup"><span data-stu-id="7bc78-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="7bc78-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bc78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bc78-105">A série de ações a seguir descreve como transportes usam os métodos TNEF para processar as mensagens de entrada e saídas.</span><span class="sxs-lookup"><span data-stu-id="7bc78-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="7bc78-106">**Para enviar uma mensagem que inclui um stream TNEF**</span><span class="sxs-lookup"><span data-stu-id="7bc78-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="7bc78-107">Processe as propriedades de mensagem que são suportadas pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7bc78-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="7bc78-108">Marca a mensagem em uma implementação específica de maneira para que o provedor de transporte de recebimento possa determinar de que a mensagem requer processamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="7bc78-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="7bc78-109">Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagem SMTP pode adicionar um campo de cabeçalho personalizado como "X-contém-TNEF" para indicar que a mensagem contém dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="7bc78-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="7bc78-110">Obter um objeto TNEF e usá-lo para encapsular as propriedades da mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="7bc78-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="7bc78-111">Codifica fluxo TNEF, usando o modelo de anexo do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7bc78-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="7bc78-112">Por exemplo, se o modelo de anexo subjacente é uuencode anexos e acrescentá-las para o texto da mensagem, o provedor de transporte deve uuencode stream TNEF em outro anexo.</span><span class="sxs-lookup"><span data-stu-id="7bc78-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="7bc78-113">O provedor de transporte também deve implementar um método para reconhecendo qual anexo contém o fluxo TNEF codificado quando ele recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bc78-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="7bc78-114">A maneira padrão para marcar este anexo é dê a ela um nome de arquivo de anexo de "WINMAIL. DAT".</span><span class="sxs-lookup"><span data-stu-id="7bc78-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="7bc78-115">Se o seu provedor de transporte faz isso, outros provedores de transporte habilitado TNEF que seguem Esta convenção poderão interoperar com ele.</span><span class="sxs-lookup"><span data-stu-id="7bc78-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="7bc78-116">Uso [ITnef: IUnknown](itnefiunknown.md) métodos para inserir marcações descrevendo as posições das anexos de mensagens no texto da mensagem de interface.</span><span class="sxs-lookup"><span data-stu-id="7bc78-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="7bc78-117">Acessar o texto da mensagem marcados por meio dos métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e enviá-la para o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7bc78-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="7bc78-118">**Para recuperar as propriedades encapsuladas**</span><span class="sxs-lookup"><span data-stu-id="7bc78-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="7bc78-119">Gravar as propriedades suportadas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem sinalizada que contém as propriedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="7bc78-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="7bc78-120">Decodificar o fluxo TNEF do anexo adequado.</span><span class="sxs-lookup"><span data-stu-id="7bc78-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="7bc78-121">Decodificar qualquer outro anexo e anotá-las para novos anexos de MAPI em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bc78-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="7bc78-122">Abra o fluxo TNEF para decodificação usando a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc78-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="7bc78-123">Use o método [ITnef::ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas para a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bc78-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="7bc78-124">Todas as propriedades codificadas duplicatas das propriedades nonencoded substituirá as propriedades nonencoded quando as propriedades codificadas são decodificadas.</span><span class="sxs-lookup"><span data-stu-id="7bc78-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="7bc78-125">Use o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar as posições de anexo das marcas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7bc78-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

