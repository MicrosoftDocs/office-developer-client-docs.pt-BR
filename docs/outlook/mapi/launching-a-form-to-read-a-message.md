---
title: Iniciando uma forma para ler uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 675de7eeda534d8761887cdcb6d5c94a209ca18b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767764"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="62aca-103">Iniciando uma forma para ler uma mensagem</span><span class="sxs-lookup"><span data-stu-id="62aca-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="62aca-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="62aca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="62aca-105">Implementadores de servidor do formulário devem esperar que a seguinte sequência de chamadas de método para seus servidores do formulário e seus objetos de formulário quando um aplicativo cliente carrega uma mensagem:</span><span class="sxs-lookup"><span data-stu-id="62aca-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="62aca-106">O aplicativo cliente abre o Gerenciador de formulário com uma chamada para a função [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="62aca-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="62aca-107">O aplicativo cliente chama o método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , que retorna um objeto com [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="62aca-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="62aca-108">O gerente de formulário pode ser lançado agora se ela não será usada para outras ativações de formulário.</span><span class="sxs-lookup"><span data-stu-id="62aca-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="62aca-109">Observe que uma chamada para **LoadForm** pode levar algum tempo porque o Gerenciador de formulário talvez seja necessário instalar os arquivos executáveis do servidor formulário antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="62aca-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="62aca-110">Opcionalmente, o aplicativo cliente pode preparar [IMAPIViewContext](imapiviewcontextiunknown.md) para controlar operações que podem causar o objeto de formulário carregar a mensagem anterior ou seguinte na pasta.</span><span class="sxs-lookup"><span data-stu-id="62aca-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="62aca-111">O aplicativo cliente pode usar o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) para alterar o contexto de modo de exibição padrão que foi definido na chamada **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="62aca-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="62aca-112">O aplicativo cliente chama o método [IPersistMessage::Load](ipersistmessage-load.md) para carregar dados de mensagem no objeto form.</span><span class="sxs-lookup"><span data-stu-id="62aca-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="62aca-113">O aplicativo cliente chama [IMAPIForm::DoVerb](imapiform-doverb.md) para invocar o verbo open, passando o ponteiro de interface [IMAPIViewContext](imapiviewcontextiunknown.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="62aca-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="62aca-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="62aca-114">See also</span></span>



[<span data-ttu-id="62aca-115">Interações do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="62aca-115">Form Server Interactions</span></span>](form-server-interactions.md)

