---
title: Integrando o código do servidor de formulário MAPI ao código do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332176"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a><span data-ttu-id="a8a9d-103">Integrando o código do servidor de formulário MAPI ao código do Windows</span><span class="sxs-lookup"><span data-stu-id="a8a9d-103">Integrating MAPI Form Server Code with Windows Code</span></span>

  
  
<span data-ttu-id="a8a9d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8a9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8a9d-105">Lembre-se de que seu servidor de formulário é um aplicativo Win32.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-105">Recall that your form server is a Win32 application.</span></span> <span data-ttu-id="a8a9d-106">Dessa forma, há algumas tarefas relacionadas ao carregamento do servidor de formulário na memória e ao sair corretamente.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-106">As such, there are some tasks related to loading your form server into memory and exiting cleanly.</span></span> <span data-ttu-id="a8a9d-107">Como todos os aplicativos do Windows, o ponto de entrada para seu servidor de formulário é a **função WinMain.**</span><span class="sxs-lookup"><span data-stu-id="a8a9d-107">Like all Windows applications, the entry point for your form server is the **WinMain** function.</span></span> <span data-ttu-id="a8a9d-108">Esta função é o local apropriado para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a8a9d-108">This function is the appropriate place to perform the following tasks:</span></span> 
  
- <span data-ttu-id="a8a9d-109">Criar e registrar uma classe de janela para que o servidor de formulário possa interagir com outros componentes OLE.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-109">Creating and registering a window class so that your form server can interact with other OLE components.</span></span>
    
- <span data-ttu-id="a8a9d-110">Criando e registrando uma classe de janela ou classes para as interfaces de usuário dos objetos de formulário.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-110">Creating and registering a window class or classes for your form objects' user interfaces.</span></span>
    
- <span data-ttu-id="a8a9d-111">Chamando a [função MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="a8a9d-111">Calling the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="a8a9d-112">**MAPIInitialize** também lida com a inicialização OLE necessária para você.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-112">**MAPIInitialize** handles the required OLE initialization for you, as well.</span></span> <span data-ttu-id="a8a9d-113">Isso deve ser feito uma vez por instância do seu servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-113">This must be done once per instance of your form server.</span></span> 
    
- <span data-ttu-id="a8a9d-114">Registrando um atom global com uma representação de cadeia de caracteres do identificador de classe do servidor de formulário (CLSID).</span><span class="sxs-lookup"><span data-stu-id="a8a9d-114">Registering a global atom with a string representation of the form server's class identifier (CLSID).</span></span> <span data-ttu-id="a8a9d-115">Esse atom deve existir durante o tempo de vida do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-115">This atom should exist for the lifetime of the form server.</span></span>
    
- <span data-ttu-id="a8a9d-116">Chamar a função OLE [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) para registrar a fábrica de classe do servidor de formulário com OLE.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-116">Calling the OLE function [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) to register your form server's class factory with OLE.</span></span> 
    
- <span data-ttu-id="a8a9d-117">Criar uma janela principal para receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-117">Creating a main window to receive messages.</span></span> <span data-ttu-id="a8a9d-118">Essa janela provavelmente não precisa estar visível porque o usuário interagirá com as janelas específicas associadas a objetos de formulário individuais.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-118">This window probably does not need to be visible because the user will be interacting with the specific windows associated with individual form objects.</span></span> <span data-ttu-id="a8a9d-119">No entanto, durante o desenvolvimento, a janela principal pode ser um local conveniente para depurar a saída ou o controle do servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-119">However, during development, the main window can be a convenient place for debugging output or control of your form server.</span></span>
    
- <span data-ttu-id="a8a9d-120">Criar um loop de mensagem que é executado durante o tempo de vida do servidor de formulário, traduzindo e expedindo mensagens do Windows para objetos de formulário ativos.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-120">Creating a message loop that runs for the lifetime of the form server, translating and dispatching windows messages to active form objects.</span></span>
    
<span data-ttu-id="a8a9d-121">Quando o servidor de formulário é final, ele deve executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="a8a9d-121">When your form server exits, it should perform the following tasks:</span></span>
  
- <span data-ttu-id="a8a9d-122">Chame a função OLE [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) para revogar o registro OLE da classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-122">Call the OLE function [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) to revoke your message class's OLE registration.</span></span> 
    
- <span data-ttu-id="a8a9d-123">Chame **MAPIUninitialize** para fechar corretamente a conexão do servidor de formulário com MAPI.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-123">Call **MAPIUninitialize** to properly close the form server's connection to MAPI.</span></span> 
    
- <span data-ttu-id="a8a9d-124">Exclua o atom global que contém a representação de cadeia de caracteres do identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="a8a9d-124">Delete the global atom that contains the string representation of the class identifier.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8a9d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8a9d-125">See also</span></span>



[<span data-ttu-id="a8a9d-126">Escrevendo código do servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="a8a9d-126">Writing Form Server Code</span></span>](writing-form-server-code.md)

