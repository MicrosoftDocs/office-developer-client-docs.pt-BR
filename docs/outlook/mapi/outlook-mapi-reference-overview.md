---
title: Visão geral da referência de MAPI do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificação: 1 de fevereiro de 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348493"
---
# <a name="outlook-mapi-reference-overview"></a><span data-ttu-id="10337-103">Visão geral da referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="10337-103">Outlook MAPI Reference Overview</span></span>

<span data-ttu-id="10337-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10337-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10337-105">Este tópico fornece informações gerais sobre a documentação de referência de MAPI do Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="10337-105">This topic provides overview information about the Outlook 2013 MAPI Reference documentation.</span></span>
  
## <a name="about-this-documentation"></a><span data-ttu-id="10337-106">A respeito desta documentação</span><span class="sxs-lookup"><span data-stu-id="10337-106">About this documentation</span></span>

<span data-ttu-id="10337-107">Esta documentação se aplica à implementação da API de mensagens (MAPI) no Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="10337-107">This documentation applies to the implementation of the Messaging API (MAPI) in Microsoft Outlook 2013.</span></span> 
  
<span data-ttu-id="10337-108">Antes do Microsoft Office Outlook 2007, a Referência para o programador de MAPI fazia parte da documentação do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="10337-108">Previous to Microsoft Office Outlook 2007, the MAPI Programmer's Reference was part of the Microsoft Exchange documentation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="10337-109">Como o Exchange reduziu a ênfase no uso de MAPI desde o Microsoft Exchange Server 2007, o suporte para a implementação do Exchange ficou limitado.</span><span class="sxs-lookup"><span data-stu-id="10337-109">Because Exchange has deemphasized the use of MAPI since Microsoft Exchange Server 2007, support for the Exchange implementation is limited.</span></span> 
  
<span data-ttu-id="10337-110">A implementação de MAPI do Outlook é diferente em relação à do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="10337-110">The Outlook implementation of MAPI differs from the Microsoft Exchange implementation.</span></span> <span data-ttu-id="10337-111">A implementação do Outlook é otimizada para execução em computadores cliente e enfatiza a baixa latência.</span><span class="sxs-lookup"><span data-stu-id="10337-111">The Outlook implementation is optimized for running on client computers and emphasizes low latency.</span></span> <span data-ttu-id="10337-112">A implementação do Exchange se destina aos servidores em que uma alta disponibilidade e vários threads melhores são importantes.</span><span class="sxs-lookup"><span data-stu-id="10337-112">The Exchange implementation is intended for servers where high availability and better multithreading are important.</span></span>
  
<span data-ttu-id="10337-113">Use esta documentação para aplicativos em execução nos sistemas de usuários finais.</span><span class="sxs-lookup"><span data-stu-id="10337-113">Use this documentation for applications running on end-user systems.</span></span> <span data-ttu-id="10337-114">No caso de aplicativos para servidores, use a implementação de MAPI do Exchange, caso adequado, ou as APIs atuais do Exchange, como os Serviços Web do Exchange.</span><span class="sxs-lookup"><span data-stu-id="10337-114">For server applications, use the Exchange implementation of MAPI if appropriate, or use current Exchange APIs such as Exchange Web Services.</span></span> <span data-ttu-id="10337-115">Para saber mais sobre os Serviços Web do Exchange, confira [Referência de Serviços Web do Exchange](https://msdn.microsoft.com/library/bb204119.aspx).</span><span class="sxs-lookup"><span data-stu-id="10337-115">For more information on Exchange Web Services, see the [Exchange Web Services Reference](https://msdn.microsoft.com/library/bb204119.aspx).</span></span>
  
<span data-ttu-id="10337-116">Talvez seja possível criar aplicativos que funcionem com as implementações de MAPI do Outlook ou do Exchange.</span><span class="sxs-lookup"><span data-stu-id="10337-116">It may be possible to write applications that work with either the Outlook or Exchange implementations of MAPI.</span></span> <span data-ttu-id="10337-117">Por exemplo, MFCMAPI funciona adequadamente em qualquer plataforma.</span><span class="sxs-lookup"><span data-stu-id="10337-117">For example, MFCMAPI works well on either platform.</span></span> <span data-ttu-id="10337-118">As implementações têm muitos recursos comuns, mas há diferenças óbvias e sutis.</span><span class="sxs-lookup"><span data-stu-id="10337-118">The implementations have many common features, but there are differences both obvious and subtle.</span></span> <span data-ttu-id="10337-119">Teste cuidadosamente nas duas plataformas, caso deseje que o aplicativo funcione em todos os ambientes.</span><span class="sxs-lookup"><span data-stu-id="10337-119">You will have to test carefully on both platforms if you intend for your application to work in all environments.</span></span> <span data-ttu-id="10337-120">Este teste exigirá dois sistemas porque não há suporte para a execução de duas implementações na mesma instalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="10337-120">This testing will require two systems because running both implementations on the same operating system installation is not supported.</span></span>
  
<span data-ttu-id="10337-121">Lembre-se de que a MAPI é apropriada para o acesso de baixo nível aos dados em um armazenamento MAPI ou para a criação de um provedor de catálogo de endereços, de transporte ou de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="10337-121">Be aware that MAPI is appropriate for low-level access to data in a MAPI store or for building a transport, message store, or address book provider.</span></span> <span data-ttu-id="10337-122">Como o MAPI ignora a lógica comercial do Outlook, considere também o uso do modelo de objeto do Outlook, quando avaliar as APIs para a criação da solução.</span><span class="sxs-lookup"><span data-stu-id="10337-122">Because MAPI bypasses Outlook's business logic, you should also consider the use of the Outlook object model when you evaluate APIs for building your solution.</span></span> <span data-ttu-id="10337-123">O modelo de objeto do Outlook encapsula a lógica comercial do Outlook, mas não é adequado para o código de vários threads, para provedores de sincronização nem para aplicativos de serviço Windows.</span><span class="sxs-lookup"><span data-stu-id="10337-123">The Outlook object model does encapsulate Outlook business logic but is not suitable for multithreaded code, sync providers, or Windows Service applications.</span></span>
  
<span data-ttu-id="10337-124">Saiba mais sobre as novidades desta edição nos tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="10337-124">For information about what is new in this edition, see the following topics:</span></span>
  
- [<span data-ttu-id="10337-125">Novidades desta edição</span><span class="sxs-lookup"><span data-stu-id="10337-125">What's New in This Edition</span></span>](what-s-new-in-this-edition.md)
    
- [<span data-ttu-id="10337-126">Elementos de API preteridos nesta edição</span><span class="sxs-lookup"><span data-stu-id="10337-126">API Elements Deprecated in This Edition</span></span>](api-elements-deprecated-in-this-edition.md)
    
<span data-ttu-id="10337-127">Se você estiver começando a desenvolver aplicativos MAPI para o Outlook, confira os tópicos a seguir:</span><span class="sxs-lookup"><span data-stu-id="10337-127">If you are new to developing MAPI applications for Outlook, see the following topics:</span></span>
  
- [<span data-ttu-id="10337-128">Escolher uma API ou tecnologia para o desenvolvimento de soluções para o Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="10337-128">Selecting an API or technology for developing solutions for Outlook 2013</span></span>](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [<span data-ttu-id="10337-129">Arquivos de cabeçalho usados com frequência</span><span class="sxs-lookup"><span data-stu-id="10337-129">Commonly Used Header Files</span></span>](commonly-used-header-files.md)
    
- [<span data-ttu-id="10337-130">Propriedades usadas com frequência</span><span class="sxs-lookup"><span data-stu-id="10337-130">Commonly Used Properties</span></span>](commonly-used-properties.md)
    
- [<span data-ttu-id="10337-131">Objetos usados com frequência</span><span class="sxs-lookup"><span data-stu-id="10337-131">Commonly Used Objects</span></span>](commonly-used-objects.md)
    
<span data-ttu-id="10337-132">O restante dessa referência é categorizado nos três tipos de informações a seguir:</span><span class="sxs-lookup"><span data-stu-id="10337-132">The rest of this reference is categorized into the following three types of information:</span></span>
  
- <span data-ttu-id="10337-133">[Exemplos de MAPI](mapi-samples.md): direciona você para muitos exemplos de código que mostram o uso de vários elementos de API, como implementar provedores MAPI básicos e criar itens do Outlook.</span><span class="sxs-lookup"><span data-stu-id="10337-133">[MAPI Samples](mapi-samples.md) - Directs you to many code samples that show the use of various API elements and how to implement basic MAPI providers and create Outlook items.</span></span> 
    
- <span data-ttu-id="10337-134">[Conceitos de MAPI](mapi-concepts.md): explica a arquitetura e os conceitos de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10337-134">[MAPI Concepts](mapi-concepts.md) - Explains the concepts and architecture of MAPI.</span></span> 
    
- <span data-ttu-id="10337-135">[Referência de MAPI](mapi-reference.md): fornece informações detalhadas sobre as funções, interfaces, estruturas e propriedades no MAPI.</span><span class="sxs-lookup"><span data-stu-id="10337-135">[MAPI Reference](mapi-reference.md) - Provides detailed information about the functions, interfaces, structures, and properties in MAPI.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="10337-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="10337-136">See also</span></span>

- [<span data-ttu-id="10337-137">Introdução à Referência de MAPI do Outlook</span><span class="sxs-lookup"><span data-stu-id="10337-137">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)
- [<span data-ttu-id="10337-138">Amostras de MAPI</span><span class="sxs-lookup"><span data-stu-id="10337-138">MAPI Samples</span></span>](mapi-samples.md)
- [<span data-ttu-id="10337-139">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="10337-139">MAPI Concepts</span></span>](mapi-concepts.md)

