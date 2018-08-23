---
title: Interfaces de formulário MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f37d398167e8210a2fd67ff08e63572eb6c9db9c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585721"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="06fa0-103">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="06fa0-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="06fa0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06fa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06fa0-105">MAPI define as seguintes interfaces relacionadas aos formulários.</span><span class="sxs-lookup"><span data-stu-id="06fa0-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="06fa0-106">**Nome da interface**</span><span class="sxs-lookup"><span data-stu-id="06fa0-106">**Interface name**</span></span>|<span data-ttu-id="06fa0-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="06fa0-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06fa0-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="06fa0-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="06fa0-109">Manipula a objetos de formulário e trata comandos de objeto do formulário.</span><span class="sxs-lookup"><span data-stu-id="06fa0-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="06fa0-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="06fa0-111">Determina se o objeto de formulário pode manipular a próxima mensagem e altera o estado anterior ou seguinte do objeto form.</span><span class="sxs-lookup"><span data-stu-id="06fa0-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="06fa0-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="06fa0-113">Oferece suporte à instalação, desinstalação e resolução de servidores de formulário contra um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="06fa0-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="06fa0-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="06fa0-115">Suporta o uso de servidores de formulário configurável de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="06fa0-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="06fa0-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="06fa0-117">Permite que aplicativos de cliente trabalhar com propriedades que são específicas para uma classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="06fa0-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="06fa0-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="06fa0-119">Permite que os aplicativos de cliente obter mais informações sobre servidores de formulário, ativa a servidores de formulário e instala os servidores de formulário no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="06fa0-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="06fa0-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="06fa0-121">Usado para manipular mensagens associadas com objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="06fa0-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="06fa0-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="06fa0-123">Notifica os aplicativos cliente que ocorreu um evento no objeto form.</span><span class="sxs-lookup"><span data-stu-id="06fa0-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="06fa0-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="06fa0-125">Usada para responder aos comandos próximo, anterior e excluir o objeto form.</span><span class="sxs-lookup"><span data-stu-id="06fa0-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="06fa0-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="06fa0-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="06fa0-127">Usado para salvar, inicializar e carregar os objetos de formulário de e para armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="06fa0-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="06fa0-128">Para obter mais informações sobre os métodos das interfaces do formulário MAPI, consulte a documentação para essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="06fa0-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="06fa0-129">Você não precisará implementar todas as interfaces de formulário MAPI para criar um formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="06fa0-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="06fa0-130">Um formulário em si só requer que você implementar a **IPersistMessage**, **IMAPIForm**, e **IMAPIFormAdviseSink** interfaces.</span><span class="sxs-lookup"><span data-stu-id="06fa0-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="06fa0-131">Além disso, também é uma boa ideia implementar **IMAPIFormFactory** e **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="06fa0-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="06fa0-132">**IMAPIFormFactory** é útil para fins de conformidade de OLE e **IMAPIFormInfo** permite que os aplicativos de cliente bem escrito tornar o melhor uso dos seus formulários.</span><span class="sxs-lookup"><span data-stu-id="06fa0-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="06fa0-133">Rigor, **IMAPIFormAdviseSink** é uma interface opcional.</span><span class="sxs-lookup"><span data-stu-id="06fa0-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="06fa0-134">No entanto, é altamente recomendável que você implemente-la em seus servidores do formulário.</span><span class="sxs-lookup"><span data-stu-id="06fa0-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="06fa0-135">Esta interface é fundamental para a interação eficiente entre clientes de mensagens e servidores de formulário, especialmente quando várias mensagens do seu servidor de formulário classe de mensagem estão sendo resolvido com.</span><span class="sxs-lookup"><span data-stu-id="06fa0-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06fa0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="06fa0-136">See also</span></span>



[<span data-ttu-id="06fa0-137">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="06fa0-137">MAPI Forms</span></span>](mapi-forms.md)

