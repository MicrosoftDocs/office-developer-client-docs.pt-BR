---
title: Texto da mensagem marcado por TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1d514dc8b50183e5d07d71b421a441487e933580
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588857"
---
# <a name="tnef-tagged-message-text"></a><span data-ttu-id="ee62a-103">Texto da mensagem marcado por TNEF</span><span class="sxs-lookup"><span data-stu-id="ee62a-103">TNEF-Tagged Message Text</span></span>

  
  
<span data-ttu-id="ee62a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee62a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee62a-105">Texto da mensagem marcados é usado pelo TNEF resolver posições de anexo na mensagem pai.</span><span class="sxs-lookup"><span data-stu-id="ee62a-105">Tagged message text is used by TNEF to resolve attachment positions in the parent message.</span></span> <span data-ttu-id="ee62a-106">Isso é feito com a adição de um espaço reservado no texto da mensagem na posição do anexo.</span><span class="sxs-lookup"><span data-stu-id="ee62a-106">This is done by adding a place holder in the message text at the position of the attachment.</span></span> <span data-ttu-id="ee62a-107">Esse espaço reservado ou marca de anexo, descreve o anexo de tal forma que o TNEF Saiba como resolver o anexo e sua posição.</span><span class="sxs-lookup"><span data-stu-id="ee62a-107">This place holder, or attachment tag, describes the attachment in such a way that TNEF knows how to resolve the attachment and its position.</span></span> <span data-ttu-id="ee62a-108">As marcas são formatadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ee62a-108">The tags are formatted as follows:</span></span>
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 <span data-ttu-id="ee62a-109">** \<Título do objeto\> ** e ** \<nome de arquivo\> ** são variáveis que contêm valores que são extraídos do anexo em si.</span><span class="sxs-lookup"><span data-stu-id="ee62a-109">**\<Object Title\>** and **\<File Name\>** are variables containing values that are taken from the attachment itself.</span></span> <span data-ttu-id="ee62a-110">Em casos onde esses valores não estão disponíveis, o título assume o padrão por TNEF com base no tipo de anexo.</span><span class="sxs-lookup"><span data-stu-id="ee62a-110">In cases where these values are not available, the title is defaulted by TNEF based on the attachment type.</span></span> 
  
<span data-ttu-id="ee62a-111">O ** \<KeyNum\> ** variável contém a representação textual da chave anexo atribuída ao anexo por TNEF.</span><span class="sxs-lookup"><span data-stu-id="ee62a-111">The **\<KeyNum\>** variable contains the textual representation of the attachment key assigned to the attachment by TNEF.</span></span> <span data-ttu-id="ee62a-112">O valor base da chave é passado na chamada de [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ee62a-112">The base value of the key is passed into the [OpenTnefStreamEx](opentnefstreamex.md) call.</span></span> <span data-ttu-id="ee62a-113">O valor de base não deve ser zero e não deve ser o mesmo para cada chamada para **OpenTnefStreamEx**.</span><span class="sxs-lookup"><span data-stu-id="ee62a-113">The base value must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="ee62a-114">Ele deve ser suficiente para usar números aleatórios de falsos baseados a hora do sistema de qualquer gerador de números aleatórios fornece em sua biblioteca de tempo de execução, desde que você garante que nunca são zero.</span><span class="sxs-lookup"><span data-stu-id="ee62a-114">It should suffice to use pseudo random numbers based on the system time from whatever random number generator your run-time library provides, as long as you guarantee that they are never zero.</span></span>
  
<span data-ttu-id="ee62a-115">O ** \<nome transporte\> ** variável contém o nome de fluxo passado para a chamada de [OpenTnefStreamEx](opentnefstreamex.md) ou o valor da propriedade **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ee62a-115">The **\<Transport Name\>** variable contains either the stream name passed into the [OpenTnefStreamEx](opentnefstreamex.md) call or the value of the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ee62a-116">A propriedade **PR_ATTACH_TRANSPORT_NAME** e o ** \<nome transporte\> ** variável em uma marca de texto da mensagem não tem nada a ver com o nome do provedor de transporte que você estiver implementando.</span><span class="sxs-lookup"><span data-stu-id="ee62a-116">The **PR_ATTACH_TRANSPORT_NAME** property and the **\<Transport Name\>** variable in a message text tag have nothing to do with the name of the transport provider you are implementing.</span></span> <span data-ttu-id="ee62a-117">Esses itens representam o nome de um anexo para o provedor de transporte e o sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee62a-117">These items represent the name of an attachment for the transport provider and messaging system.</span></span> 
  
<span data-ttu-id="ee62a-118">O texto da mensagem está marcado quando um provedor de transporte solicita um texto de mensagem marcados chamando o método [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="ee62a-118">The message text is tagged when a transport provider asks for a tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="ee62a-119">Ao ler a partir do fluxo de texto marcado, o TNEF substituirá o caractere único que estava no texto da mensagem no índice fornecido na propriedade **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) com a marca apropriada.</span><span class="sxs-lookup"><span data-stu-id="ee62a-119">When reading from the tagged text stream, TNEF replaces the single character that was in the message text at the index provided in the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property with the appropriate tag.</span></span> <span data-ttu-id="ee62a-120">Ao gravar o fluxo de texto marcado, TNEF verifica os dados de entrada de marcas, localiza o anexo associado e substitui a marca com um caractere de espaço simples.</span><span class="sxs-lookup"><span data-stu-id="ee62a-120">When writing to the tagged text stream, TNEF checks the incoming data for tags, finds the associated attachment, and replaces the tag with a single space character.</span></span>
  
<span data-ttu-id="ee62a-121">Observe que, usando o texto da mensagem marcados, um provedor de transporte pode preservar o posicionamento de anexos independentemente da maioria das alterações feitas para o texto da mensagem por sistemas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ee62a-121">Note that by using tagged message text, a transport provider can preserve the positioning of attachments regardless of most changes made to the message text by messaging systems.</span></span>
  

