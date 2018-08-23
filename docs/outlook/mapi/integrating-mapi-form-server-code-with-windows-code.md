---
title: Integrar o código do servidor de formulário MAPI ao código do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b37ae47e40906342aeecf179848311556a7d4ba4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573989"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="93be8-103">Integrar o código do servidor de formulário MAPI ao código do Windows</span><span class="sxs-lookup"><span data-stu-id="93be8-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="93be8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93be8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93be8-105">Lembre-se de que seu servidor de formulário é um aplicativo Win32.</span><span class="sxs-lookup"><span data-stu-id="93be8-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="93be8-106">Assim, há algumas tarefas relacionadas ao carregar o seu servidor de formulário na memória e saindo corretamente.</span><span class="sxs-lookup"><span data-stu-id="93be8-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="93be8-107">Como todos os aplicativos do Windows, o ponto de entrada para seu servidor de formulário é a função **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="93be8-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="93be8-108">Essa função é o local adequado para realizar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="93be8-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="93be8-109">Criar e registrar uma classe de janela para que seu servidor de formulário possa interagir com outros componentes do OLE.</span><span class="sxs-lookup"><span data-stu-id="93be8-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="93be8-110">Criar e registrar uma classe de janela ou classes para interfaces do usuário dos objetos do formulário.</span><span class="sxs-lookup"><span data-stu-id="93be8-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="93be8-111">Chamar a função de [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="93be8-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="93be8-112">**MAPIInitialize** trata a OLE inicialização necessária para você, também.</span><span class="sxs-lookup"><span data-stu-id="93be8-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="93be8-113">Isso deve ser feito uma vez por instância do seu servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="93be8-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="93be8-114">Registrando um atom global com uma representação de cadeia de caracteres de identificador do servidor formulário de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="93be8-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="93be8-115">Este atom deve existir para o tempo de vida do servidor do formulário.</span><span class="sxs-lookup"><span data-stu-id="93be8-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="93be8-116">Chamar a função OLE [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) para registrar o alocador de classe do seu servidor de formulário com OLE.</span><span class="sxs-lookup"><span data-stu-id="93be8-116">Calling the OLE function [CoRegisterClassObject](http://msdn.microsoft.com/en-us/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="93be8-117">Criando uma janela principal para receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="93be8-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="93be8-118">Essa janela provavelmente não precisa estar visível porque o usuário interagirá com as janelas específicas associadas a objetos de formulário individuais.</span><span class="sxs-lookup"><span data-stu-id="93be8-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="93be8-119">No entanto, durante o desenvolvimento, a janela principal pode ser um local conveniente para controle do seu servidor do formulário ou saída de depuração.</span><span class="sxs-lookup"><span data-stu-id="93be8-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="93be8-120">Criando um loop de mensagem que é executado para o tempo de vida do servidor do formulário, traduzindo e expedir mensagens do windows para objetos do formulário ativo.</span><span class="sxs-lookup"><span data-stu-id="93be8-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="93be8-121">Quando seu servidor de formulário é encerrado, ele deve executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="93be8-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="93be8-122">Chame a função OLE [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) para revogar o registro do OLE da classe da mensagem.</span><span class="sxs-lookup"><span data-stu-id="93be8-122">Call the OLE function [CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="93be8-123">Chame **MAPIUninitialize** para fechar corretamente a conexão do servidor de formulário para MAPI.</span><span class="sxs-lookup"><span data-stu-id="93be8-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="93be8-124">Exclua o atom global que contém a representação de cadeia de caracteres do identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="93be8-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93be8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="93be8-125">See also</span></span>



[<span data-ttu-id="93be8-126">Gravar um código de servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="93be8-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

