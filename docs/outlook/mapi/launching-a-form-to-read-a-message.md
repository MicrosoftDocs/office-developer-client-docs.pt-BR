---
title: Iniciar um formulário para ler uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 439927dc78941f086c025d77c76236497d3f4a15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307809"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="7f5f3-103">Iniciar um formulário para ler uma mensagem</span><span class="sxs-lookup"><span data-stu-id="7f5f3-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="7f5f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f5f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f5f3-105">Os implementadores do servidor de formulários devem esperar a seguinte sequência de chamadas de método para o servidor de formulários e os objetos de formulário quando um aplicativo cliente carrega uma mensagem:</span><span class="sxs-lookup"><span data-stu-id="7f5f3-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="7f5f3-106">O aplicativo cliente abre o Gerenciador de formulários com uma chamada para a função [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="7f5f3-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="7f5f3-107">O aplicativo cliente chama o método [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) , que retorna um objeto com [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="7f5f3-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="7f5f3-108">O Gerenciador de formulários pode ser liberado agora se não for usado para ativações de formulários adicionais.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="7f5f3-109">Observe que uma chamada para **loadform** pode levar algum tempo porque o Gerenciador de formulários pode ter que instalar os arquivos executáveis do servidor de formulário antes de prosseguir.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="7f5f3-110">Opcionalmente, o aplicativo cliente pode preparar o [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar as operações que podem fazer com que o objeto Form carregue a mensagem anterior ou seguinte na pasta.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="7f5f3-111">O aplicativo cliente pode usar o método [IMAPIForm:: SetViewContext](imapiform-setviewcontext.md) para alterar o contexto de exibição padrão definido na chamada loadform. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7f5f3-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="7f5f3-112">O aplicativo cliente chama o método [IPersistMessage:: Load](ipersistmessage-load.md) para carregar dados de mensagem no objeto Form.</span><span class="sxs-lookup"><span data-stu-id="7f5f3-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="7f5f3-113">O aplicativo cliente chama [IMAPIForm::D overb](imapiform-doverb.md) para invocar o verbo Open, passando o ponteiro de interface opcional do [IMAPIViewContext](imapiviewcontextiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7f5f3-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7f5f3-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f5f3-114">See also</span></span>



[<span data-ttu-id="7f5f3-115">InterAções do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="7f5f3-115">Form Server Interactions</span></span>](form-server-interactions.md)

