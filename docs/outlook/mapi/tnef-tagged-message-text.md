---
title: Texto da mensagem marcado como TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339589"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="1fc7d-103">Texto da mensagem marcado como TNEF</span><span class="sxs-lookup"><span data-stu-id="1fc7d-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="1fc7d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fc7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fc7d-105">O texto da mensagem marcada é usado pelo TNEF para resolver posições de anexo na mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="1fc7d-106">Isso é feito adicionando um espaço reservado no texto da mensagem na posição do anexo.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="1fc7d-107">Este espaço reservado, ou marca de anexo, descreve o anexo de tal forma que o TNEF sabe como resolver o anexo e sua posição.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="1fc7d-108">As marcas são formatadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1fc7d-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="1fc7d-109">O título \*\* \<\> \*\* do objeto e o nome do arquivo são variáveis que contêm valores que são obtidos do próprio anexo. \*\* \<\> \*\*</span><span class="sxs-lookup"><span data-stu-id="1fc7d-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="1fc7d-110">Nos casos em que esses valores não estão disponíveis, o título é padronizado por TNEF com base no tipo de anexo.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="1fc7d-111">A \*\* \<variável\> KeyNum\*\* contém a representação textual da chave de anexo atribuída ao anexo por TNEF.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="1fc7d-112">O valor base da chave é passado para a chamada [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc7d-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="1fc7d-113">O valor base não deve ser zero e não deve ser o mesmo para todas as chamadas para **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="1fc7d-114">Deve ser suficiente usar números pseudo aleatórios com base no tempo do sistema de qualquer gerador de número aleatório que sua biblioteca de tempo de execução fornece, desde que você garanta que eles nunca sejam zero.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="1fc7d-115">A \*\* \<variável de\> nome de transporte\*\* contém o nome do fluxo passado para a chamada [OpenTnefStreamEx](opentnefstreamex.md) ou o valor da propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1fc7d-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1fc7d-116">A propriedade **PR_ATTACH_TRANSPORT_NAME** e a \*\* \<variável de\> nome de transporte\*\* em uma marca de texto de mensagem não têm nada a ver com o nome do provedor de transporte que você está implementando.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="1fc7d-117">Estes itens representam o nome de um anexo para o provedor de transporte e o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="1fc7d-118">O texto da mensagem é marcado quando um provedor de transporte solicita um texto da mensagem marcada chamando o método [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="1fc7d-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="1fc7d-119">Ao ler a partir do fluxo de texto marcado, o TNEF substitui o caractere único que estava no texto da mensagem no índice fornecido na propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) com a marca apropriada.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="1fc7d-120">Ao gravar no fluxo de texto marcado, o TNEF verifica os dados de entrada para marcas, localiza o anexo associado e substitui a marca por um único caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="1fc7d-121">Observe que, usando o texto da mensagem marcada, um provedor de transporte pode preservar o posicionamento de anexos, independentemente da maioria das alterações feitas no texto da mensagem pelos sistemas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1fc7d-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

