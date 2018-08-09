---
title: Elementos de API preteridos nesta edição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766168"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="cbd18-103">Elementos de API preteridos nesta edição</span><span class="sxs-lookup"><span data-stu-id="cbd18-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="cbd18-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbd18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbd18-105">Os seguintes elementos de API são reduzidos no Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="cbd18-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="cbd18-106">Eles não são mais suportados e você não deve usá-los em novos projetos.</span><span class="sxs-lookup"><span data-stu-id="cbd18-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="cbd18-107">Preterir da mensagem e destinatários opções</span><span class="sxs-lookup"><span data-stu-id="cbd18-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="cbd18-108">Os seguintes elementos de API são preteridos nesta versão devido a mensagem obsoleta e opções de destinatário:</span><span class="sxs-lookup"><span data-stu-id="cbd18-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="cbd18-109">**IXPLogon::RegisterOptions**— subsistema de MAPI não são mais chama esse método para estabelecer a todos os valores padrão para as opções de mensagem e destinatário para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="cbd18-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="cbd18-110">**OPTIONDATA**— essa estrutura de dados que suporte a propriedades para as opções de mensagem e destinatário é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="cbd18-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="cbd18-111">O subsistema de MAPI não são mais chama **IXPLogon::RegisterOptions** para obter qualquer mensagem ou opções de destinatário que oferece suporte a um provedor de transporte para um tipo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="cbd18-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="cbd18-112">**OPTIONCALLBACK**— esse protótipo de função para um provedor de transporte usado para declarar uma função de retorno de chamada e que, por sua vez, o subsistema MAPI usado para resolver as propriedades do provedor, é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="cbd18-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="cbd18-113">Não há mais o subsistema MAPI chama **IXPLogon::RegisterOptions** ou usa qualquer função de retorno de chamada retornada pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="cbd18-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="cbd18-114">**IMAPISession::MessageOptions**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para exibir as propriedades ou permitir que os usuários definir propriedades que controlam um determinado tipo de mensagem e o endereço.</span><span class="sxs-lookup"><span data-stu-id="cbd18-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="cbd18-115">O método sempre retornará E_NOT_FOUND, que indica que não há nenhuma opção de mensagem para a mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="cbd18-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="cbd18-116">**IMAPISession::QueryDefaultMessageOpt**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para recuperar as propriedades que controlam as opções de mensagem para um tipo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="cbd18-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="cbd18-117">O método não retorna um ponteiro para qualquer conjunto de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="cbd18-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="cbd18-118">**IAddrBook::RecipOptions**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para exibir as propriedades ou permitir que os usuários definir propriedades que o processamento de controle para um destinatário de um tipo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="cbd18-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="cbd18-119">O método sempre retornará MAPI_W_ERRORS_RETURNED, que indica que não existem opções destinatários para o destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="cbd18-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="cbd18-120">**IAddrBook::QueryDefaultRecipOpt**— provedores MAPI de cliente e o serviço não são mais devem chamar esse método para recuperar as propriedades que controlam as opções de destinatário para um tipo de endereço específica.</span><span class="sxs-lookup"><span data-stu-id="cbd18-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="cbd18-121">O método não retorna um ponteiro para qualquer conjunto de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="cbd18-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cbd18-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbd18-122">See also</span></span>



[<span data-ttu-id="cbd18-123">Introdução à Referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="cbd18-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

