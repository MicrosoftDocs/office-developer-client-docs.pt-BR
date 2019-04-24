---
title: Práticas recomendadas para o desenvolvimento de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Você deve cumprir as seguintes práticas ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281234"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="96704-103">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="96704-103">Best practices for developing a provider</span></span>

<span data-ttu-id="96704-104">Você deve cumprir as seguintes práticas ao desenvolver um provedor do Outlook Social Connector 2013 (OSC):</span><span class="sxs-lookup"><span data-stu-id="96704-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="96704-105">Por motivos de segurança, os provedores que se comunicam com servidores pela Internet devem usar o protocolo HTTPS (Hypertext Transfer Protocol (HTTP) com Secure Socket Layer (SSL)).</span><span class="sxs-lookup"><span data-stu-id="96704-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="96704-106">Caso contrário, há um risco de que endereços de email, atividades de rede social e outros dados de usuário possam ser interceptados ou expostos enquanto estão em trânsito.</span><span class="sxs-lookup"><span data-stu-id="96704-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="96704-107">Se você estiver desenvolvendo um provedor do OSC para uma rede social de terceiros, seu provedor deve cumprir os termos de serviço da rede social.</span><span class="sxs-lookup"><span data-stu-id="96704-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="96704-108">Para minimizar o tamanho do pacote de download do provedor, crie o provedor usando um compilador nativo como C++ ou qualquer outra ferramenta que possa criar um componente COM.</span><span class="sxs-lookup"><span data-stu-id="96704-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="96704-109">Em seu provedor, crie um agente de usuário exclusivo que é enviado para a rede social para rastrear as chamadas feitas pelo provedor para a rede social.</span><span class="sxs-lookup"><span data-stu-id="96704-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="96704-110">O método [ISocialProvider:: GetCapabilities](isocialprovider-getcapabilities.md) não deve depender de chamar a rede social pela Internet para obter os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="96704-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="96704-111">Por exemplo, os usuários podem iniciar o Outlook offline; Se o OSC chamar **GetCapabilities** e não houver conexão de rede, a \*\*\*\* chamada GetCapabilities não retornará XML de **recursos** válidos.</span><span class="sxs-lookup"><span data-stu-id="96704-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="96704-112">A prática recomendada é armazenar o XML de **recursos** como um recurso no provedor.</span><span class="sxs-lookup"><span data-stu-id="96704-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="96704-113">O provedor do OSC pode gerar um volume significativo de chamadas para uma rede social.</span><span class="sxs-lookup"><span data-stu-id="96704-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="96704-114">Dependendo dos termos de serviço da sua rede social, considere o armazenamento em cache de amigos para uma pasta do Outlook a fim de reduzir o número de chamadas do OSC para o seu provedor e, por sua vez, de seu provedor para a rede social.</span><span class="sxs-lookup"><span data-stu-id="96704-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="96704-115">O Office 2013 está disponível nas versões de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="96704-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="96704-116">As versões do Office anteriores ao Office 2010 estão disponíveis somente em uma versão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="96704-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="96704-117">A instalação padrão do Office 2013 no Windows de 64 bits é de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="96704-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="96704-118">Se você pretende oferecer suporte à versão de 64 bits do OSC que é instalada com o Office de 64 bits 2013, você também deve liberar uma versão de 64 bits do provedor.</span><span class="sxs-lookup"><span data-stu-id="96704-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="96704-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="96704-119">See also</span></span>

- [<span data-ttu-id="96704-120">Sequências de chamada típicas do OSC</span><span class="sxs-lookup"><span data-stu-id="96704-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="96704-121">Desenvolver um provedor com o esquema XML do OSC</span><span class="sxs-lookup"><span data-stu-id="96704-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="96704-122">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="96704-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="96704-123">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="96704-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

