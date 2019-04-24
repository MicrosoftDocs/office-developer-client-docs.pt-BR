---
title: Desenvolver servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338525"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="b6f32-103">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="b6f32-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="b6f32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6f32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6f32-105">Esta seção descreve o processo de criação de arquivos executáveis e de configuração de formulário do servidor de formulários para a criação de formulários MAPI personalizados.</span><span class="sxs-lookup"><span data-stu-id="b6f32-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="b6f32-106">Antes de ler esta seção, familiarize-se com as informações em [formulários MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="b6f32-107">O desenvolvimento de um servidor de formulários inclui as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b6f32-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="b6f32-108">Decidir quais informações o formulário conterá e escolher um conjunto de propriedades para manter essas informações.</span><span class="sxs-lookup"><span data-stu-id="b6f32-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="b6f32-109">Para obter mais informações, consulte [escolhendo o conjunto de propriedades de um formulário](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="b6f32-110">Criar uma interface do usuário com a qual os usuários podem interagir com as propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="b6f32-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="b6f32-111">Escolher uma classe de mensagem e gerar um identificador de classe exclusivo (CLSID).</span><span class="sxs-lookup"><span data-stu-id="b6f32-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="b6f32-112">Para obter uma visão geral das classes de mensagens, consulte [MAPI Message classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="b6f32-113">Para obter mais informações sobre classes e formulários de mensagens, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="b6f32-114">Implementar as interfaces de formulário MAPI necessárias, bem como qualquer interface opcional que seu servidor de formulário específico precise.</span><span class="sxs-lookup"><span data-stu-id="b6f32-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="b6f32-115">Para obter mais informações, consulte [Writing Form Server Code](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="b6f32-116">Escrever o código de interface do usuário para lidar com a interação do usuário com o objeto Form e as propriedades que o formulário usa.</span><span class="sxs-lookup"><span data-stu-id="b6f32-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="b6f32-117">Criar um arquivo de configuração de formulário para o formulário.</span><span class="sxs-lookup"><span data-stu-id="b6f32-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="b6f32-118">Para obter mais informações, consulte [formato de arquivo dos arquivos de configuração de formulário](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="b6f32-119">Instalar o formulário nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="b6f32-119">Installing the form on users' computers.</span></span> <span data-ttu-id="b6f32-120">Para obter mais informações, consulte [instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="b6f32-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="b6f32-121">Você provavelmente executará as etapas de 1 a 5 simultaneamente, em vez de concluí-las em sequência.</span><span class="sxs-lookup"><span data-stu-id="b6f32-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="b6f32-122">O processo de desenvolvimento de um servidor de formulários, como muitos projetos de programação, não é um no qual há uma sequência muito bem definida.</span><span class="sxs-lookup"><span data-stu-id="b6f32-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="b6f32-123">Por exemplo, a criação de um arquivo de configuração de formulário é mostrada como a segunda etapa acima, mas você provavelmente criará o arquivo de configuração de formulário de forma incremental e se tornará mais completo à medida que você adicionar recursos ao servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="b6f32-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6f32-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6f32-124">See also</span></span>



[<span data-ttu-id="b6f32-125">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="b6f32-125">MAPI Concepts</span></span>](mapi-concepts.md)

