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
# <a name="tnef-processing"></a><span data-ttu-id="6b6e1-103">Processamento TNEF</span><span class="sxs-lookup"><span data-stu-id="6b6e1-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="6b6e1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b6e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b6e1-105">A série de ações a seguir descrevem como os transportes usam métodos TNEF para processar mensagens de saída e de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="6b6e1-106">**Para enviar uma mensagem que inclui um fluxo TNEF**</span><span class="sxs-lookup"><span data-stu-id="6b6e1-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="6b6e1-107">Processe as propriedades da mensagem que são suportadas pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="6b6e1-108">Marcar a mensagem em uma forma específica de implementação para que o provedor de transporte de recebimento possa determinar que a mensagem requer processamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="6b6e1-109">Por exemplo, um provedor de transporte TNEF enviando para um sistema de mensagens SMTP pode adicionar um campo de cabeçalho personalizado como "X-CONTAINS-TNEF" para indicar que a mensagem contém dados TNEF.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="6b6e1-110">Obtenha um objeto TNEF e use-o para encapsular as propriedades de mensagem não suportadas pelo sistema de mensagens em um fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="6b6e1-111">Codifique o fluxo TNEF usando o modelo de anexo do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="6b6e1-112">Por exemplo, se o modelo de anexo subjacente for uuencode anexos e acrescentá-los ao texto da mensagem, o provedor de transporte deverá uuencode o fluxo TNEF para outro anexo.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="6b6e1-113">O provedor de transporte também deve implementar um método para reconhecer qual anexo contém o fluxo TNEF codificado quando recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="6b6e1-114">O modo padrão de marcar esse anexo é dar a ele um nome de arquivo de anexo de "WINMAIL. DAT ".</span><span class="sxs-lookup"><span data-stu-id="6b6e1-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="6b6e1-115">Se o seu provedor de transporte fizer isso, todos os outros provedores de transporte habilitados para TNEF que seguirem essa Convenção poderão interoperar com ele.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="6b6e1-116">Use os métodos de interface [ITnef: IUnknown](itnefiunknown.md) para inserir marcas descrevendo as posições dos anexos de mensagens no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="6b6e1-117">Acessar o texto da mensagem marcada por meio de métodos [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e enviá-lo ao sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="6b6e1-118">**Para recuperar propriedades encapsuladas**</span><span class="sxs-lookup"><span data-stu-id="6b6e1-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="6b6e1-119">Escreva as propriedades aceitas pelo sistema de mensagens em uma nova mensagem, incluindo o texto da mensagem marcada que contém as propriedades encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="6b6e1-120">DeCodifique o fluxo TNEF do anexo adequado.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="6b6e1-121">DeCodifique quaisquer outros anexos e grave-os em novos anexos MAPI em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="6b6e1-122">Abra o fluxo TNEF para decodificação usando a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="6b6e1-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="6b6e1-123">Use o método [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar o fluxo TNEF e gravar as propriedades encapsuladas na nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="6b6e1-124">Quaisquer propriedades codificadas que sejam duplicatas de propriedades não codificadas substituirão as propriedades não codificadas quando as propriedades codificadas forem decodificadas.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="6b6e1-125">Use o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) para analisar o texto da mensagem para recuperar posições de anexo das marcas no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6b6e1-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

