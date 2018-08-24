---
title: Desenvolver servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d55134cf5181ebbba0108c228d9afc3a494e75ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576236"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="63971-103">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="63971-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="63971-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63971-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63971-105">Esta seção descreve o processo de criação de servidor do formulário executável e arquivos de configuração de formulário para a criação de formulários personalizados de MAPI.</span><span class="sxs-lookup"><span data-stu-id="63971-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="63971-106">Antes de ler esta seção, familiarize-se com as informações nos [Formulários de MAPI](mapi-forms.md).</span><span class="sxs-lookup"><span data-stu-id="63971-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="63971-107">Desenvolver um servidor de formulário inclui as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="63971-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="63971-108">Decidindo quais informações que conterá o formulário e escolhendo um conjunto de propriedades para armazenar essas informações.</span><span class="sxs-lookup"><span data-stu-id="63971-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="63971-109">Para obter mais informações, consulte [Escolher o conjunto de propriedade de um formulário](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="63971-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="63971-110">Projetando uma interface de usuário com a qual os usuários podem interagir com as propriedades do formulário.</span><span class="sxs-lookup"><span data-stu-id="63971-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="63971-111">Escolhendo uma classe de mensagem e gerar um identificador exclusivo de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="63971-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="63971-112">Para obter uma visão geral das classes de mensagem, consulte [Classes de mensagem MAPI](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="63971-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="63971-113">Para obter mais informações sobre formulários e classes de mensagens, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="63971-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="63971-114">Implementando as interfaces de formulário MAPI necessárias, bem como qualquer interfaces opcionais que precisa de seu servidor de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="63971-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="63971-115">Para obter mais informações, consulte [à escrita de código de servidor de formulário](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="63971-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="63971-116">Como escrever o código de interface do usuário para manipular a interação do usuário com o objeto de formulário e as propriedades usa o formulário.</span><span class="sxs-lookup"><span data-stu-id="63971-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="63971-117">Criando um arquivo de configuração de formulário para o formulário.</span><span class="sxs-lookup"><span data-stu-id="63971-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="63971-118">Para obter mais informações, consulte o [Arquivo de formato do formulário arquivos de configuração](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="63971-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="63971-119">Instalando o formulário nos computadores dos usuários.</span><span class="sxs-lookup"><span data-stu-id="63971-119">Installing the form on users' computers.</span></span> <span data-ttu-id="63971-120">Para obter mais informações, consulte [Instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="63971-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="63971-121">Provavelmente você executará as etapas 1 a 5 simultaneamente em vez de concluí-las em uma sequência.</span><span class="sxs-lookup"><span data-stu-id="63971-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="63971-122">O processo de desenvolvimento de um servidor de formulário, como muitos projetos de programação, não é um nos quais houver uma sequência particularmente bem definida.</span><span class="sxs-lookup"><span data-stu-id="63971-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="63971-123">Por exemplo, criar um arquivo de configuração do formulário é mostrado como a segundo a última etapa acima, mas você provavelmente irá criar seu arquivo de configuração do formulário incrementalmente e tornarão mais completa conforme você adicionar recursos ao seu servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="63971-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="63971-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="63971-124">See also</span></span>



[<span data-ttu-id="63971-125">Conceitos MAPI</span><span class="sxs-lookup"><span data-stu-id="63971-125">MAPI Concepts</span></span>](mapi-concepts.md)

