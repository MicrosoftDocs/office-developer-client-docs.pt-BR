---
title: Desenvolvendo servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420763"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="86ee6-103">Desenvolvendo servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="86ee6-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="86ee6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86ee6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86ee6-105">Esta seção descreve o processo de criação de arquivos executáveis de servidor de formulários e de configuração de formulários para a criação de formulários MAPI personalizados.</span><span class="sxs-lookup"><span data-stu-id="86ee6-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="86ee6-106">Antes de ler esta seção, você deve se familiarizar com as informações nos [formulários MAPI.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="86ee6-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="86ee6-107">O desenvolvimento de um servidor de formulário inclui as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="86ee6-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="86ee6-108">Decidir quais informações o formulário conterá e escolher um conjunto de propriedades para manter essas informações.</span><span class="sxs-lookup"><span data-stu-id="86ee6-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="86ee6-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="86ee6-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="86ee6-110">Projetar uma interface do usuário com a qual os usuários podem interagir com as propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="86ee6-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="86ee6-111">Escolher uma classe de mensagem e gerar um identificador de classe exclusivo (CLSID).</span><span class="sxs-lookup"><span data-stu-id="86ee6-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="86ee6-112">Para uma visão geral das classes de mensagens, consulte [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="86ee6-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="86ee6-113">Para obter mais informações sobre classes de mensagens e formulários, consulte [Escolhendo uma classe de mensagem.](choosing-a-message-class.md)</span><span class="sxs-lookup"><span data-stu-id="86ee6-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="86ee6-114">Implementando as interfaces de formulário MAPI necessárias, bem como quaisquer interfaces opcionais que seu servidor de formulário específico precisa.</span><span class="sxs-lookup"><span data-stu-id="86ee6-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="86ee6-115">Para obter mais informações, consulte [Escrevendo código do servidor de formulário.](writing-form-server-code.md)</span><span class="sxs-lookup"><span data-stu-id="86ee6-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="86ee6-116">Escrevendo o código da interface do usuário para manipular a interação do usuário com o objeto de formulário e as propriedades que o formulário usa.</span><span class="sxs-lookup"><span data-stu-id="86ee6-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="86ee6-117">Criando um arquivo de configuração de formulário para o formulário.</span><span class="sxs-lookup"><span data-stu-id="86ee6-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="86ee6-118">Para obter mais informações, consulte [Formato de arquivo de arquivos de configuração de formulário.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="86ee6-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="86ee6-119">Instalando o formulário nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="86ee6-119">Installing the form on users' computers.</span></span> <span data-ttu-id="86ee6-120">Para obter mais informações, [consulte Instalando um formulário em uma biblioteca.](installing-a-form-into-a-library.md)</span><span class="sxs-lookup"><span data-stu-id="86ee6-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="86ee6-121">Você provavelmente executará as etapas de 1 a 5 simultaneamente, em vez de concluí-las em sequência.</span><span class="sxs-lookup"><span data-stu-id="86ee6-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="86ee6-122">O processo de desenvolvimento de um servidor de formulário, como muitos projetos de programação, não é aquele em que há uma sequência particularmente bem definida.</span><span class="sxs-lookup"><span data-stu-id="86ee6-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="86ee6-123">Por exemplo, a criação de um arquivo de configuração de formulário é mostrada como a segunda até a última etapa acima, mas você provavelmente criará seu arquivo de configuração de formulário incrementalmente e ele se tornará mais completo à medida que você adicionar recursos ao servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="86ee6-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="86ee6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="86ee6-124">See also</span></span>



[<span data-ttu-id="86ee6-125">Conceitos de MAPI</span><span class="sxs-lookup"><span data-stu-id="86ee6-125">MAPI Concepts</span></span>](mapi-concepts.md)

