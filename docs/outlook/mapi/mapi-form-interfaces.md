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
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412342"
---
# <a name="mapi-form-interfaces"></a><span data-ttu-id="402e2-103">Interfaces de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="402e2-103">MAPI Form Interfaces</span></span>

  
  
<span data-ttu-id="402e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="402e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="402e2-105">MAPI define as interfaces a seguir relacionadas aos formulários.</span><span class="sxs-lookup"><span data-stu-id="402e2-105">MAPI defines the following interfaces relating to forms.</span></span>
  
|<span data-ttu-id="402e2-106">**Nome da interface**</span><span class="sxs-lookup"><span data-stu-id="402e2-106">**Interface name**</span></span>|<span data-ttu-id="402e2-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="402e2-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="402e2-108">IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="402e2-108">IMAPIForm</span></span>](imapiformiunknown.md) <br/> |<span data-ttu-id="402e2-109">Manipula objetos de formulário e manipula comandos de objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="402e2-109">Manipulates form objects and handles form object commands.</span></span>  <br/> |
|[<span data-ttu-id="402e2-110">IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="402e2-110">IMAPIFormAdviseSink</span></span>](imapiformadvisesinkiunknown.md) <br/> |<span data-ttu-id="402e2-111">Determina se o objeto de formulário pode manipular a próxima mensagem e altera o estado seguinte ou anterior do objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="402e2-111">Determines if the form object can handle the next message and changes the next or previous state of the form object.</span></span>  <br/> |
|[<span data-ttu-id="402e2-112">IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="402e2-112">IMAPIFormContainer</span></span>](imapiformcontaineriunknown.md) <br/> |<span data-ttu-id="402e2-113">Oferece suporte à instalação, desinstalação e resolução de servidores de formulário em relação a um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="402e2-113">Supports installation, deinstallation, and resolution of form servers against a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="402e2-114">IMAPIFormFactory</span><span class="sxs-lookup"><span data-stu-id="402e2-114">IMAPIFormFactory</span></span>](imapiformfactoryiunknown.md) <br/> |<span data-ttu-id="402e2-115">Oferece suporte ao uso de servidores de formulário de tempo de executar configuráveis.</span><span class="sxs-lookup"><span data-stu-id="402e2-115">Supports the use of configurable run-time form servers.</span></span>  <br/> |
|[<span data-ttu-id="402e2-116">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="402e2-116">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md) <br/> |<span data-ttu-id="402e2-117">Permite que os aplicativos cliente trabalhem com propriedades específicas de uma classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="402e2-117">Enables client applications to work with properties that are specific to a message class.</span></span>  <br/> |
|[<span data-ttu-id="402e2-118">IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="402e2-118">IMAPIFormMgr</span></span>](imapiformmgriunknown.md) <br/> |<span data-ttu-id="402e2-119">Permite que os aplicativos clientes recebam informações sobre servidores de formulário, ativem servidores de formulário e instalem servidores de formulário no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="402e2-119">Enables client applications to get information about form servers, activates form servers, and installs form servers in the messaging system.</span></span>  <br/> |
|[<span data-ttu-id="402e2-120">IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="402e2-120">IMAPIMessageSite</span></span>](imapimessagesiteiunknown.md) <br/> |<span data-ttu-id="402e2-121">Usado para manipular mensagens associadas a objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="402e2-121">Used to manipulate messages associated with form objects.</span></span>  <br/> |
|[<span data-ttu-id="402e2-122">IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="402e2-122">IMAPIViewAdviseSink</span></span>](imapiviewadvisesinkiunknown.md) <br/> |<span data-ttu-id="402e2-123">Notifica os aplicativos cliente de que ocorreu um evento no objeto form.</span><span class="sxs-lookup"><span data-stu-id="402e2-123">Notifies client applications that an event has occurred in the form object.</span></span>  <br/> |
|[<span data-ttu-id="402e2-124">IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="402e2-124">IMAPIViewContext</span></span>](imapiviewcontextiunknown.md) <br/> |<span data-ttu-id="402e2-125">Usado para responder aos comandos Next, Previous e Delete no objeto form.</span><span class="sxs-lookup"><span data-stu-id="402e2-125">Used to respond to Next, Previous, and Delete commands in the form object.</span></span>  <br/> |
|[<span data-ttu-id="402e2-126">IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="402e2-126">IPersistMessage</span></span>](ipersistmessageiunknown.md) <br/> |<span data-ttu-id="402e2-127">Usado para salvar, inicializar e carregar objetos de formulário de e para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="402e2-127">Used to save, initialize, and load form objects to and from message storage.</span></span>  <br/> |
   
<span data-ttu-id="402e2-128">Para obter mais informações sobre os métodos das interfaces de formulário MAPI, consulte a documentação dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="402e2-128">For more information about the methods of the MAPI form interfaces, see the documentation for these interfaces.</span></span> <span data-ttu-id="402e2-129">Você não precisa implementar todas as interfaces de formulário MAPI para criar um formulário personalizado.</span><span class="sxs-lookup"><span data-stu-id="402e2-129">You do not have to implement all of the MAPI form interfaces in order to create a custom form.</span></span> <span data-ttu-id="402e2-130">Um formulário em si exige apenas que você implemente as interfaces **IPersistMessage**, **IMAPIForm** e **IMAPIFormAdviseSink.**</span><span class="sxs-lookup"><span data-stu-id="402e2-130">A form itself requires only that you implement the **IPersistMessage**, **IMAPIForm**, and **IMAPIFormAdviseSink** interfaces.</span></span> <span data-ttu-id="402e2-131">Além disso, também é uma boa ideia implementar **IMAPIFormFactory** e **IMAPIFormInfo**.</span><span class="sxs-lookup"><span data-stu-id="402e2-131">Additionally, it is also a good idea to implement **IMAPIFormFactory** and **IMAPIFormInfo**.</span></span> <span data-ttu-id="402e2-132">**IMAPIFormFactory** é útil para conformidade OLE, e **IMAPIFormInfo** permite que aplicativos cliente bem escritos usem melhor seus formulários.</span><span class="sxs-lookup"><span data-stu-id="402e2-132">**IMAPIFormFactory** is useful for OLE compliance, and **IMAPIFormInfo** enables well-written client applications to make better use of your forms.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="402e2-133">A rigor, **IMAPIFormAdviseSink** é uma interface opcional.</span><span class="sxs-lookup"><span data-stu-id="402e2-133">Strictly speaking, **IMAPIFormAdviseSink** is an optional interface.</span></span> <span data-ttu-id="402e2-134">No entanto, é altamente recomendável implementá-lo em seus servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="402e2-134">However, it is strongly recommended that you implement it in your form servers.</span></span> <span data-ttu-id="402e2-135">Essa interface é essencial para uma interação eficiente entre clientes de mensagens e servidores de formulário, especialmente quando várias mensagens da classe de mensagens do seu servidor de formulário estão sendo tratadas.</span><span class="sxs-lookup"><span data-stu-id="402e2-135">This interface is critical to efficient interaction between messaging clients and form servers, especially when several messages of your form server's message class are being dealt with.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="402e2-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="402e2-136">See also</span></span>



[<span data-ttu-id="402e2-137">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="402e2-137">MAPI Forms</span></span>](mapi-forms.md)

