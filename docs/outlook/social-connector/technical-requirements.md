---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM e requisitos de método de retorno e os detalhes da extensibilidade DLL do provedor Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329152"
---
# <a name="technical-requirements"></a><span data-ttu-id="8216d-103">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="8216d-103">Technical requirements</span></span>

<span data-ttu-id="8216d-104">Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM e requisitos de método de retorno e os detalhes da extensibilidade DLL do provedor Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="8216d-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="8216d-105">Linguagem de programação e requisitos de COM</span><span class="sxs-lookup"><span data-stu-id="8216d-105">Programming language and COM requirements</span></span>

<span data-ttu-id="8216d-106">Você pode criar um provedor OSC usando idiomas gerenciados como visuais c# ou o Visual Basic ou idiomas não gerenciados como Visual C++.</span><span class="sxs-lookup"><span data-stu-id="8216d-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="8216d-107">Você pode usar qualquer ferramenta de que possa criar um componente DLL COM visível para desenvolver um provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="8216d-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="8216d-108">A decisão de usar uma linguagem gerenciada ou não gerenciada para desenvolver um provedor deve levar em conta o tamanho do download e dependências do pacote de instalação do provedor.</span><span class="sxs-lookup"><span data-stu-id="8216d-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="8216d-109">Um provedor de OSC deve estar COM visível conforme definido pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="8216d-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="8216d-110">Após a instalação, um provedor de OSC deve ser registrado usando registro COM automático ou regsvr32.</span><span class="sxs-lookup"><span data-stu-id="8216d-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="8216d-111">Registro COM de um provedor OSC DLL de registra o provedor em HKCU ou HKLM.</span><span class="sxs-lookup"><span data-stu-id="8216d-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="8216d-112">Registrado em ProgID um provedor `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="8216d-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="8216d-113">Um provedor de OSC desenvolvido em um idioma gerenciado é COM visível.</span><span class="sxs-lookup"><span data-stu-id="8216d-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="8216d-114">Um provedor de OSC deve adicionar valores no registro do Windows que indicam que o provedor DLL dá suporte tanto para os modelos de compartimento thread (STA) quanto para o compartimento multithread (MTA).</span><span class="sxs-lookup"><span data-stu-id="8216d-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="8216d-115">Para mais informações sobre modelos COM de threading, confira[descrições e o funcionamento do modelo OLE Threading](https://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="8216d-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](https://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="8216d-116">Métodos de extensibilidade do provedor OSC devem retornar tipos primitivos como **cadeia de caracteres** ou **bool**.</span><span class="sxs-lookup"><span data-stu-id="8216d-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="8216d-117">Determinadas **cadeias** que retornam valores devem ser compatíveis com a definição do esquema de extensibilidade provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="8216d-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="8216d-118">Apenas XML é aceito como um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8216d-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="8216d-119">Detalhes da extensibilidade OSC provedor DLL</span><span class="sxs-lookup"><span data-stu-id="8216d-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="8216d-120">O componente que suporta a extensibilidade do provedor OSC é a extensibilidade OSC do provedor DLL.</span><span class="sxs-lookup"><span data-stu-id="8216d-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="8216d-121">Desenvolvedores terceiros podem criar o OSC do provedor DLLs usando essas extensibilidade de interfaces.</span><span class="sxs-lookup"><span data-stu-id="8216d-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="8216d-122">A lista a seguir mostra os detalhes da extensibilidade OSC do provedor DLL:</span><span class="sxs-lookup"><span data-stu-id="8216d-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="8216d-123">Nome do arquivo extensibilidade DLL: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="8216d-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="8216d-124">Nome amigável da extensibilidade DLL: Microsoft Outlook Social provedor extensibilidade</span><span class="sxs-lookup"><span data-stu-id="8216d-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="8216d-125">Versão principal do extensibilidade DLL: 15.0</span><span class="sxs-lookup"><span data-stu-id="8216d-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="8216d-126">Versão Extensibiilty DLL TypeLib: 1.1</span><span class="sxs-lookup"><span data-stu-id="8216d-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="8216d-127">Informações técnicas diversas</span><span class="sxs-lookup"><span data-stu-id="8216d-127">Miscellaneous technical information</span></span>

<span data-ttu-id="8216d-128">JSON (JavaScript Object Notation) não é suportada no modelo de extensibilidade OSC provedor.</span><span class="sxs-lookup"><span data-stu-id="8216d-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="8216d-129">Não há nenhuma dependência no analisador de XML.</span><span class="sxs-lookup"><span data-stu-id="8216d-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="8216d-130">O provedor do OSC pode usar um analisador XML que está incluído no Office, e também o Microsoft XML Core Services (MSXML), usar os recursos de análise do XML integrado ao Microsoft .NET Framework ou usar um analisador XML de terceiros.</span><span class="sxs-lookup"><span data-stu-id="8216d-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8216d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8216d-131">See also</span></span>

- [<span data-ttu-id="8216d-132">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="8216d-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="8216d-133">Etapas rápidas para aprender a desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="8216d-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="8216d-134">Implantar um provedor</span><span class="sxs-lookup"><span data-stu-id="8216d-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="8216d-135">Introdução ao desenvolvimento de um provedor de serviços do Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="8216d-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

