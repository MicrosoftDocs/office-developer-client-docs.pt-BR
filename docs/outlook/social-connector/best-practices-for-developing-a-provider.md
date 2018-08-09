---
title: Práticas recomendadas para o desenvolvimento de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Você deve aderir às práticas a seguir ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770819"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="b6851-103">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="b6851-103">Best practices for developing a provider</span></span>

<span data-ttu-id="b6851-104">Você deve aderir às práticas a seguir ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):</span><span class="sxs-lookup"><span data-stu-id="b6851-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="b6851-105">Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com a camada de soquete seguro (SSL)).</span><span class="sxs-lookup"><span data-stu-id="b6851-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="b6851-106">Caso contrário, há um risco que endereços de email, atividades de redes sociais e outro usuário dados poderiam ser interceptados ou expostos em trânsito.</span><span class="sxs-lookup"><span data-stu-id="b6851-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="b6851-107">Se você estiver desenvolvendo um provedor OSC para uma rede social de terceiros, seu provedor deve aderir ao termos da rede social de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6851-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="b6851-108">Para minimizar o tamanho do pacote de download do provedor, crie o provedor usando um compilador nativo como C++ ou qualquer outra ferramenta que pode construir um componente COM.</span><span class="sxs-lookup"><span data-stu-id="b6851-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="b6851-109">Em seu provedor, crie um agente de usuário exclusiva que será enviado para a rede social para controlar as chamadas feitas pelo provedor à rede social.</span><span class="sxs-lookup"><span data-stu-id="b6851-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="b6851-110">O método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) não deve confiar em chamadas da rede social na Internet para obter os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="b6851-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="b6851-111">Por exemplo, os usuários podem iniciar o Outlook offline; Se o OSC chama **GetCapabilities** e não há nenhuma conexão de rede, a chamada **GetCapabilities** não retornará válido **recursos** XML.</span><span class="sxs-lookup"><span data-stu-id="b6851-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="b6851-112">A prática recomendada é armazenar **recursos** XML como um recurso em seu provedor.</span><span class="sxs-lookup"><span data-stu-id="b6851-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="b6851-113">Seu provedor OSC pode gerar um volume significativo de chamadas para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="b6851-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="b6851-114">Dependendo dos termos de serviço para a sua rede social, considere a possibilidade de cache amigos para uma pasta do Outlook para reduzir o número de chamadas do seu provedor de OSC e, em seguida, do seu provedor à rede social.</span><span class="sxs-lookup"><span data-stu-id="b6851-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="b6851-115">Office 2013 está disponível nas versões de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b6851-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="b6851-116">Versões do Office anteriores ao Office 2010 estão disponíveis apenas em uma versão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b6851-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="b6851-117">A instalação padrão do Office 2013 no Windows de 64 bits é de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b6851-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="b6851-118">Se você pretende oferecer suporte à versão de 64 bits do OSC que é instalado com o Office 2013 de 64 bits, você também deve liberar uma versão de 64 bits do seu provedor.</span><span class="sxs-lookup"><span data-stu-id="b6851-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b6851-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6851-119">See also</span></span>

- [<span data-ttu-id="b6851-120">Sequências de chamadas comuns do OSC</span><span class="sxs-lookup"><span data-stu-id="b6851-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="b6851-121">Desenvolvendo um provedor com o esquema OSC XML</span><span class="sxs-lookup"><span data-stu-id="b6851-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="b6851-122">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="b6851-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b6851-123">Introdução ao desenvolvimento de um Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="b6851-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

