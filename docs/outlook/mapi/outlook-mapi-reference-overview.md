---
title: Visão geral da referência de MAPI do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '�ltima altera��o: sexta-feira, 1 de fevereiro de 2013'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768192"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="9e5f3-103">Visão geral da referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="9e5f3-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="9e5f3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e5f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e5f3-105">Este tópico fornece informações gerais sobre a documentação de referência do MAPI do Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="9e5f3-106">Sobre esta documentação</span><span class="sxs-lookup"><span data-stu-id="9e5f3-106">About this documentation</span></span>

<span data-ttu-id="9e5f3-107">Esta documentação se aplica à implementação da API do MAPI (Messaging) no Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="9e5f3-108">Anterior para o Microsoft Office Outlook 2007, a referência do programador de MAPI fazia parte da documentação do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9e5f3-109">Porque o Exchange tem deemphasized o uso de MAPI desde o Microsoft Exchange Server 2007, o suporte para a implementação do Exchange é limitada.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="9e5f3-110">A implementação do MAPI do Outlook difere de implementação do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="9e5f3-111">A implementação do Outlook é otimizada para execução nos computadores cliente e enfatiza baixa latência.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="9e5f3-112">A implementação do Exchange é direcionada para servidores que exigem alta disponibilidade e melhor multithreading são importantes.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="9e5f3-113">Use essa documentação para aplicativos executados em sistemas de usuário final.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="9e5f3-114">Para aplicativos de servidor, use a implementação do Exchange do MAPI se apropriado ou use APIs atual do Exchange, como serviços Web do Exchange.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="9e5f3-115">Para obter mais informações sobre serviços Web do Exchange, consulte a [Referência do Exchange Web Services](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e5f3-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](http://msdn.microsoft.com/en-us/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="9e5f3-116">Talvez seja possível escrever aplicativos que funcionam com o Outlook ou o Exchange implementações de MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="9e5f3-117">Por exemplo, o MFCMAPI funciona bem em qualquer uma das plataformas.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="9e5f3-118">As implementações tem muitos recursos comuns, mas há diferenças óbvias e sutil.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="9e5f3-119">Você precisará testar cuidadosamente em ambas as plataformas, caso você pretenda para seu aplicativo funcionar em todos os ambientes.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="9e5f3-120">Esse teste exigirá dois sistemas porque não há suporte para a execução as duas implementações na mesma instalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="9e5f3-121">Lembre-se de que o MAPI é apropriado para baixo nível acesso aos dados em um repositório MAPI ou para a criação de um transporte, o armazenamento de mensagens ou o provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="9e5f3-122">Como o MAPI ignora a lógica de negócios do Outlook, você também deve considerar o uso do modelo de objeto do Outlook ao avaliar APIs para a criação de sua solução.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="9e5f3-123">O modelo de objeto do Outlook encapsulam a lógica de negócios do Outlook, mas não é adequado para código multithread, provedores de sincronização ou aplicativos de serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="9e5f3-124">Para obter informações sobre quais são as novidades nesta edição, consulte os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="9e5f3-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="9e5f3-125">Novidades nesta edi��o (em ingl�s)</span><span class="sxs-lookup"><span data-stu-id="9e5f3-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="9e5f3-126">Elementos de API preteridos nesta edi��o</span><span class="sxs-lookup"><span data-stu-id="9e5f3-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="9e5f3-127">Se você ainda não conhece para desenvolver aplicativos MAPI para Outlook, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9e5f3-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="9e5f3-128">Selecionando uma API ou tecnologia para desenvolver soluções do Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="9e5f3-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [<span data-ttu-id="9e5f3-129">Arquivos de cabe�alho usados com freq��ncia</span><span class="sxs-lookup"><span data-stu-id="9e5f3-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="9e5f3-130">Propriedades comumente usadas</span><span class="sxs-lookup"><span data-stu-id="9e5f3-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="9e5f3-131">Os objetos mais usados</span><span class="sxs-lookup"><span data-stu-id="9e5f3-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="9e5f3-132">O restante desta referência é categorizado os três tipos de informações a seguintes:</span><span class="sxs-lookup"><span data-stu-id="9e5f3-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="9e5f3-133">[Amostras de MAPI](mapi-samples.md) - direciona você para muitos exemplos de código que mostram o uso de vários elementos de API e como implementar provedores MAPI básicas e criar itens do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="9e5f3-134">[Conceitos MAPI](mapi-concepts.md) - explica os conceitos e a arquitetura do MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="9e5f3-135">[Referência MAPI](mapi-reference.md) - fornece informações detalhadas sobre as funções, interfaces, estruturas e propriedades na MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e5f3-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9e5f3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e5f3-136">See also</span></span>

- [<span data-ttu-id="9e5f3-137">Introdução à Referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="9e5f3-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="9e5f3-138">Amostras MAPI (em ingl�s)</span><span class="sxs-lookup"><span data-stu-id="9e5f3-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="9e5f3-139">Conceitos MAPI (em ingl�s)</span><span class="sxs-lookup"><span data-stu-id="9e5f3-139">MAPI Concepts</span></span>](mapi-concepts.md)

