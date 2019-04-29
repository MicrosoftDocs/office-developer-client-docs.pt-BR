---
title: Elementos de API preTeridos nesta edição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436885"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="43a16-103">Elementos de API preTeridos nesta edição</span><span class="sxs-lookup"><span data-stu-id="43a16-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="43a16-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43a16-105">Os seguintes elementos da API são preteridos no Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="43a16-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="43a16-106">Eles não são mais suportados e você não deve usá-los em novos projetos.</span><span class="sxs-lookup"><span data-stu-id="43a16-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="43a16-107">Substituição de opções de mensagens e destinatários</span><span class="sxs-lookup"><span data-stu-id="43a16-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="43a16-108">Os seguintes elementos de API são preteridos nesta versão devido às opções obsoletas de mensagem e destinatário:</span><span class="sxs-lookup"><span data-stu-id="43a16-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="43a16-109">**IXPLogon:: registeroptions**, o subsistema MAPI não chama mais este método para estabelecer qualquer valor padrão para as opções de mensagem e destinatário de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="43a16-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="43a16-110">**OPTIONDATA**— essa estrutura de dados que dá suporte a propriedades de mensagens e opções de destinatário é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="43a16-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="43a16-111">O subsistema MAPI não chama mais **IXPLogon:: registeroptions** para obter qualquer opção de mensagens ou destinatários que um provedor de transporte ofereça suporte a um determinado tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="43a16-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="43a16-112">**OPTIONCALLBACK**— este protótipo de função, que é um provedor de transporte usado para declarar uma função de retorno de chamada e que, por sua vez, o subsistema MAPI usado para resolver as propriedades do provedor, é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="43a16-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="43a16-113">O subsistema MAPI não chama mais **IXPLogon:: registeroptions** ou usa qualquer função de retorno de chamada retornada pelo provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="43a16-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="43a16-114">**IMAPISession:: messageoptions**— o cliente MAPI e os provedores de serviço não devem mais chamar este método para exibir propriedades ou permitir que os usuários definam propriedades que controlam um determinado tipo de mensagem e endereço.</span><span class="sxs-lookup"><span data-stu-id="43a16-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="43a16-115">O método sempre retorna MAPI_E_NOT_FOUND, que indica que não há opções de mensagem para a mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="43a16-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="43a16-116">**IMAPISession:: QueryDefaultMessageOpt**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para recuperar propriedades que controlam as opções de mensagem para um tipo de endereço específico.</span><span class="sxs-lookup"><span data-stu-id="43a16-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="43a16-117">O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="43a16-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="43a16-118">**IAddrBook:: RecipOptions**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para exibir propriedades ou permitir que os usuários definam propriedades que controlam o processamento de um destinatário de um determinado tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="43a16-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="43a16-119">O método sempre retorna MAPI_W_ERRORS_RETURNED, que indica que não há opções de destinatário para o destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="43a16-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="43a16-120">**IAddrBook:: QueryDefaultRecipOpt**— o cliente MAPI e os provedores de serviço não devem mais chamar esse método para recuperar propriedades que controlam as opções de destinatário para um determinado tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="43a16-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="43a16-121">O método não retorna mais um ponteiro para qualquer matriz de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="43a16-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43a16-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a16-122">See also</span></span>



[<span data-ttu-id="43a16-123">Introdução à Referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="43a16-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

