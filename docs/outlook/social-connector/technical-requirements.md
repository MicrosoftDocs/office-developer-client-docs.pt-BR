---
title: Requisitos técnicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM retornam requisitos de tipo e detalhes de DLL de extensibilidade do provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 94b57e20957f3d8d779c4d3324ecbb8ccd37f60a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770952"
---
# <a name="technical-requirements"></a><span data-ttu-id="60912-103">Requisitos técnicos</span><span class="sxs-lookup"><span data-stu-id="60912-103">Technical requirements</span></span>

<span data-ttu-id="60912-104">Este tópico descreve os idiomas com suporte de programação, método e a visibilidade COM retornam requisitos de tipo e detalhes de DLL de extensibilidade do provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="60912-104">This topic describes the supported programming languages, COM visibility and method return type requirements, and details of the Outlook Social Connector (OSC) provider extensibility DLL.</span></span> 
  
## <a name="programming-language-and-com-requirements"></a><span data-ttu-id="60912-105">Requisitos de COM e linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="60912-105">Programming language and COM requirements</span></span>

<span data-ttu-id="60912-106">Você pode criar um provedor OSC utilizando linguagens gerenciadas como Visual c# ou Visual Basic ou não gerenciado de idiomas como o Visual C++.</span><span class="sxs-lookup"><span data-stu-id="60912-106">You can create an OSC provider by using managed languages such as Visual C# or Visual Basic, or unmanaged languages such as Visual C++.</span></span> <span data-ttu-id="60912-107">Você pode usar qualquer ferramenta que pode criar um componente DLL COM visíveis para desenvolver um provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="60912-107">You can use any tool that can create a COM-visible DLL component to develop an OSC provider.</span></span> <span data-ttu-id="60912-108">A decisão de usar um idioma gerenciado ou para desenvolver um provedor deve levar em conta o tamanho do download e dependências do pacote de instalação do provedor.</span><span class="sxs-lookup"><span data-stu-id="60912-108">The decision to use a managed or unmanaged language to develop a provider should take into account the download size and dependencies of the provider installation package.</span></span>
  
<span data-ttu-id="60912-109">Um provedor OSC deve ser visível em COM, conforme definido pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="60912-109">An OSC provider must be COM-visible as defined by the following:</span></span>
  
- <span data-ttu-id="60912-110">Após a instalação, um provedor OSC deve ser registrado usando self-registro COM ou regsvr32.</span><span class="sxs-lookup"><span data-stu-id="60912-110">After installation, an OSC provider must be registered by using COM self-registration or regsvr32.</span></span>
    
- <span data-ttu-id="60912-111">Registro COM de um provedor OSC DLL registra o provedor em HKCU ou HKLM.</span><span class="sxs-lookup"><span data-stu-id="60912-111">COM registration of an OSC provider DLL registers the provider under HKCU or HKLM.</span></span> 
    
- <span data-ttu-id="60912-112">ProgID de um provedor está registrado em `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span><span class="sxs-lookup"><span data-stu-id="60912-112">A provider's ProgID is registered under  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.</span></span>
    
- <span data-ttu-id="60912-113">Um provedor OSC desenvolvido em um idioma gerenciado é visível em COM.</span><span class="sxs-lookup"><span data-stu-id="60912-113">An OSC provider developed in a managed language is COM-visible.</span></span>
    
- <span data-ttu-id="60912-114">Um provedor OSC adicione valores no registro do Windows que indicam que o provedor DLL suporta compartimento de segmentação única (STA) e o MTA (multithreaded apartment) modelos de threading.</span><span class="sxs-lookup"><span data-stu-id="60912-114">An OSC provider should add values to the Windows registry that indicate that the provider DLL supports both single-threaded apartment (STA) and multithreaded apartment (MTA) threading models.</span></span> <span data-ttu-id="60912-115">Para obter mais informações sobre o COM modelos de threading, consulte [as descrições e funcionamento de OLE Threading modelos](http://support.microsoft.com/kb/150777).</span><span class="sxs-lookup"><span data-stu-id="60912-115">For more information about COM threading models, see [Descriptions and Workings of OLE Threading Models](http://support.microsoft.com/kb/150777).</span></span>
    
<span data-ttu-id="60912-116">Métodos na extensibilidade do provedor OSC devem retornar tipos primitivos como **cadeia de caracteres** ou **bool**.</span><span class="sxs-lookup"><span data-stu-id="60912-116">Methods in OSC provider extensibility must return primitive types such as **string** or **bool**.</span></span> <span data-ttu-id="60912-117">Determinada **cadeia de caracteres** retornam valores devem estar em conformidade com a definição de esquema para fornecer extensibilidade de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="60912-117">Certain **string** return values must comply with the schema definition for OSC provider extensibility.</span></span> <span data-ttu-id="60912-118">Somente XML é aceito como um valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="60912-118">Only XML is supported as a return value.</span></span> 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a><span data-ttu-id="60912-119">Detalhes da extensibilidade do provedor OSC DLL</span><span class="sxs-lookup"><span data-stu-id="60912-119">Details of the OSC provider extensibility DLL</span></span>

<span data-ttu-id="60912-120">O componente que ofereça suporte a estensibilidade do provedor do OSC é a extensibilidade do provedor OSC DLL.</span><span class="sxs-lookup"><span data-stu-id="60912-120">The component that supports OSC provider extensibility is the OSC provider extensibility DLL.</span></span> <span data-ttu-id="60912-121">Desenvolvedores de terceiros podem criar DLLs de provedor do OSC usando essas interfaces de extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="60912-121">Third-party developers can build OSC provider DLLs by using these extensibility interfaces.</span></span> <span data-ttu-id="60912-122">A lista a seguir mostra os detalhes da extensibilidade do provedor OSC DLL:</span><span class="sxs-lookup"><span data-stu-id="60912-122">The following list shows the details of the OSC provider extensibility DLL:</span></span>
  
- <span data-ttu-id="60912-123">Nome do arquivo DLL extensibilidade: socialprovider.dll</span><span class="sxs-lookup"><span data-stu-id="60912-123">Extensibility DLL file name: socialprovider.dll</span></span>
    
- <span data-ttu-id="60912-124">Nome amigável da DLL de extensibilidade: extensibilidade do Microsoft Outlook Social provedor</span><span class="sxs-lookup"><span data-stu-id="60912-124">Extensibility DLL friendly name: Microsoft Outlook Social Provider Extensibility</span></span>
    
- <span data-ttu-id="60912-125">Versão principal de DLL de extensibilidade: 15.0</span><span class="sxs-lookup"><span data-stu-id="60912-125">Extensibility DLL major version: 15.0</span></span>
    
- <span data-ttu-id="60912-126">Versão Extensibiilty DLL TypeLib: 1.1</span><span class="sxs-lookup"><span data-stu-id="60912-126">Extensibiilty DLL TypeLib version: 1.1</span></span>
    
## <a name="miscellaneous-technical-information"></a><span data-ttu-id="60912-127">Diversas informações técnicas</span><span class="sxs-lookup"><span data-stu-id="60912-127">Miscellaneous technical information</span></span>

<span data-ttu-id="60912-128">Não há suporte para o JavaScript Object Notation (JSON) no modelo de extensibilidade do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="60912-128">JavaScript Object Notation (JSON) is not supported in the OSC provider extensibility model.</span></span>
  
<span data-ttu-id="60912-129">Não há nenhuma dependência em um analisador XML.</span><span class="sxs-lookup"><span data-stu-id="60912-129">There are no dependencies on an XML parser.</span></span> <span data-ttu-id="60912-130">O provedor do OSC pode usar um analisador XML que está incluído no Office, como o Microsoft XML Core Services (MSXML), use o recursos incorporados ao Microsoft .NET Framework de análise de XML ou usar um analisador XML de terceiros.</span><span class="sxs-lookup"><span data-stu-id="60912-130">The OSC provider can use an XML parser that is included with Office, such as Microsoft XML Core Services (MSXML), use the XML parsing capabilities built into the Microsoft .NET Framework, or use a third-party XML parser.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60912-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="60912-131">See also</span></span>

- [<span data-ttu-id="60912-132">Práticas recomendadas para o desenvolvimento de um provedor</span><span class="sxs-lookup"><span data-stu-id="60912-132">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)  
- [<span data-ttu-id="60912-133">Etapas rápidas de aprendizado para desenvolver um provedor</span><span class="sxs-lookup"><span data-stu-id="60912-133">Quick Steps for Learning to Develop a Provider</span></span>](quick-steps-for-learning-to-develop-a-provider.md)
- [<span data-ttu-id="60912-134">Implantando um provedor</span><span class="sxs-lookup"><span data-stu-id="60912-134">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="60912-135">Introdução ao desenvolvimento de um Outlook Social Connector Provider</span><span class="sxs-lookup"><span data-stu-id="60912-135">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

