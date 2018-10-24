---
title: Codificar uma mensagem com TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382523"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="2c6b5-103">Codificar uma mensagem com TNEF</span><span class="sxs-lookup"><span data-stu-id="2c6b5-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="2c6b5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c6b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c6b5-105">Quando uma mensagem é enviada, o provedor de transporte pode criar um arquivo que é usado para conter a mensagem durante a transmissão.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="2c6b5-106">Em seguida, uma interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) é disposta ao redor do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="2c6b5-107">O provedor de transporte, em seguida, usa os métodos [ITnef](itnefiunknown.md) para gravar as propriedades da mensagem fluxo em um formato marcado que permite que as propriedades a ser facilmente decodificado pelos provedores de recebimento de transporte.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="2c6b5-108">**Para representar uma mensagem inteira em um único arquivo**</span><span class="sxs-lookup"><span data-stu-id="2c6b5-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="2c6b5-109">Obter um objeto TNEF ao passar um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) e uma mensagem para a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="2c6b5-110">Obtenha uma lista de todas as propriedades definidas para a mensagem chamando o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="2c6b5-111">Use métodos [IMAPIProp](imapipropiunknown.md) para excluir todas as propriedades suportadas pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="2c6b5-112">Em um horário adequado, grave essas propriedades para o sistema de mensagens no formato exigido pelo sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="2c6b5-113">Chame [ITnef::AddProps](itnef-addprops.md) para codificar as propriedades restantes, incluindo todos os anexos.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="2c6b5-114">Chame o método [ITnef::Finish](itnef-finish.md) para codificar a mensagem no fluxo TNEF depois que todas as propriedades solicitadas são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="2c6b5-115">Chame o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) para obter o texto da mensagem marcados.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="2c6b5-116">Esse texto marcado é gravado em um sistema de mensagens usando os métodos da interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) do OLE.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="2c6b5-117">Chame o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) para liberar o objeto **ITnef** .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="2c6b5-118">**Para processar uma mensagem de entrada TNEF**</span><span class="sxs-lookup"><span data-stu-id="2c6b5-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="2c6b5-119">Obter um objeto de mensagem MAPI do spooler MAPI e propriedades de cabeçalho da mensagem de gravação para a nova mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="2c6b5-120">Criar e inicializar um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para conter os dados TNEF da mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="2c6b5-121">Passe a mensagem MAPI e o objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para a função [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="2c6b5-122">Decodificar as informações nos dados TNEF chamando o método [ITnef::ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="2c6b5-123">Nada decodificada por **ExtractProps** substituirá propriedades decodificadas do envelope da mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="2c6b5-124">Ou seja, propriedades extraídas de TNEF substituirá as propriedades existentes em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="2c6b5-125">Processar o texto da mensagem marcados chamando [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) e analisar o texto para recuperar as posições de anexo.</span><span class="sxs-lookup"><span data-stu-id="2c6b5-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="2c6b5-126">Salve a mensagem chamando [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="2c6b5-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="2c6b5-127">Libere o objeto TNEF chamando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2c6b5-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

