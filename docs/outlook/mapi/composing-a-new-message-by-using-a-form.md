---
title: Redigir uma nova mensagem usando um formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c92181c4-79ca-4310-8bf1-2bc335c8e0cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1c5ba8631ba39309b7131440f04564f80b5dbb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412797"
---
# <a name="composing-a-new-message-by-using-a-form"></a><span data-ttu-id="b218a-103">Redigir uma nova mensagem usando um formulário</span><span class="sxs-lookup"><span data-stu-id="b218a-103">Composing a New Message by Using a Form</span></span>

  
  
<span data-ttu-id="b218a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b218a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b218a-105">Para usar um formulário para redigir uma nova mensagem, primeiro crie um novo objeto Message personalizado.</span><span class="sxs-lookup"><span data-stu-id="b218a-105">To use a form to compose a new message, first create a new custom message object.</span></span>
  
 <span data-ttu-id="b218a-106">**Para redigir uma nova mensagem usando um formulário**</span><span class="sxs-lookup"><span data-stu-id="b218a-106">**To compose a new message using a form**</span></span>
  
1. <span data-ttu-id="b218a-107">Chame o método [IMAPIFormMgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md) do gerente de formulários para recuperar um ponteiro para um objeto de informações de formulário — um objeto que implementa a interface [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b218a-107">Call the form manager's [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to retrieve a pointer to a form information object — an object that implements the [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
2. <span data-ttu-id="b218a-108">Passe o ponteiro para o objeto de informações de formulário em uma chamada para [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md).</span><span class="sxs-lookup"><span data-stu-id="b218a-108">Pass the pointer to the form information object in a call to [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md).</span></span> <span data-ttu-id="b218a-109">**CreateForm** carrega o servidor de formulário apropriado.</span><span class="sxs-lookup"><span data-stu-id="b218a-109">**CreateForm** loads the appropriate form server.</span></span> <span data-ttu-id="b218a-110">Além disso, passe um identificador de interface \*\*\*\* para CreateForm para especificar a interface a ser usada para acessar a nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="b218a-110">In addition, pass an interface identifier to **CreateForm** to specify the interface to be used to access the new message.</span></span> <span data-ttu-id="b218a-111">Normalmente, você solicita [IPersistMessage: IUnknown](ipersistmessageiunknown.md) passando IID_IPersistMessage para **CreateForm**.</span><span class="sxs-lookup"><span data-stu-id="b218a-111">Typically, you request [IPersistMessage : IUnknown](ipersistmessageiunknown.md) by passing IID_IPersistMessage to **CreateForm**.</span></span>
    
3. <span data-ttu-id="b218a-112">Salve a nova mensagem chamando o método [IPersistMessage:: Save](ipersistmessage-save.md) .</span><span class="sxs-lookup"><span data-stu-id="b218a-112">Save the new message by calling its [IPersistMessage::Save](ipersistmessage-save.md) method.</span></span> <span data-ttu-id="b218a-113">O servidor de formulários deve definir valores para as propriedades obrigatórias da mensagem quando ele cria a mensagem.</span><span class="sxs-lookup"><span data-stu-id="b218a-113">The form server should set values for the message's required properties when it creates the message.</span></span> 
    
4. <span data-ttu-id="b218a-114">Carregue a mensagem usando uma das duas estratégias: [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) ou [IMAPISession::P Repareform](imapisession-prepareform.md) seguido por [IMAPISession:: o formulário](imapisession-showform.md).</span><span class="sxs-lookup"><span data-stu-id="b218a-114">Load the message by using one of two strategies: [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) or [IMAPISession::PrepareForm](imapisession-prepareform.md) followed by [IMAPISession::ShowForm](imapisession-showform.md).</span></span> <span data-ttu-id="b218a-115">Para obter mais informações sobre essas estratégias, consulte [carregar uma mensagem em um formulário](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="b218a-115">For more information about these strategies, see [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="b218a-116">Há oportunidades de ganhos de desempenho ao carregar uma nova mensagem personalizada em um servidor de formulário, pois você já terá uma oportunidade de obter algumas informações sobre a mensagem, como sua classe de mensagens, durante o processamento necessário para o \*\* \*\*Chamadas ResolveMessageClass \*\*\*\* e CreateForm.</span><span class="sxs-lookup"><span data-stu-id="b218a-116">There are opportunities for performance gains when loading a new custom message into a form server because you will already have had an opportunity to get some information about the message — such as its message class — during the processing required for the **ResolveMessageClass** and **CreateForm** calls.</span></span> <span data-ttu-id="b218a-117">Por esse motivo, você poderá simplificar o processamento necessário antes de chamar **loadform** sobre isso descrito no tópico [carregando uma mensagem em um formulário](loading-a-message-into-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="b218a-117">Because of this, you will be able to simplify the processing required before calling **LoadForm** over that described in the topic [Loading a Message Into a Form](loading-a-message-into-a-form.md).</span></span> 
  

