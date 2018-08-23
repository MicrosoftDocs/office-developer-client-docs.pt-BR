---
title: Suporte à instalação do serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1f82741e3c44c589a18a1428fd68cebe6a501d5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581990"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="3298a-103">Suporte à instalação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="3298a-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="3298a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3298a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3298a-105">O programa de instalação para instalar o serviço de mensagem deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3298a-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="3298a-106">Copie os arquivos do serviço de mensagens, como o serviço de mensagem e o provedor de serviços de DLLs, de um CD ou disco, para uma unidade local na estação de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3298a-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="3298a-107">Os arquivos que precisam ser copiados dependem de seu serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3298a-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="3298a-108">Normalmente, você irá copiar DLL pelo menos um.</span><span class="sxs-lookup"><span data-stu-id="3298a-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="3298a-109">Adicione entradas para o arquivo de configuração Mapisvc.</span><span class="sxs-lookup"><span data-stu-id="3298a-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="3298a-110">Para obter mais informações sobre como modificar esse arquivo para os provedores de serviços de suporte no seu serviço de mensagem, consulte o [Formato de arquivo do Mapisvc](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="3298a-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="3298a-111">Adicione entradas, conforme apropriado para o registro do sistema para serviços de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3298a-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="3298a-112">Para obter mais informações sobre como as entradas devem aparecer no registro do sistema, consulte [Instalando o subsistema de MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="3298a-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="3298a-113">Crie um perfil padrão, caso ainda não exista usando um dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="3298a-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="3298a-114">O Assistente de perfil para criar um perfil usando a interação do usuário através de uma série de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="3298a-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="3298a-115">Para obter mais informações sobre como usar o Assistente de perfil, consulte o [tópico Criando um perfil usando o Assistente de perfil](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="3298a-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="3298a-116">O painel de controle para criar um perfil usando a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3298a-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="3298a-117">O painel de controle oferece ao usuário mais flexibilidade do que o Assistente de perfil para configurar os serviços de mensagem e definir propriedades de perfil.</span><span class="sxs-lookup"><span data-stu-id="3298a-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="3298a-118">Coloque o programa de instalação em uma pasta pública designada.</span><span class="sxs-lookup"><span data-stu-id="3298a-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="3298a-119">Isso é importante porque a maioria dos clientes de configuração, como o painel de controle, exigem que os usuários insiram o nome do diretório.</span><span class="sxs-lookup"><span data-stu-id="3298a-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="3298a-120">O painel de controle invoca um programa de instalação quando um usuário clica no botão **Adicionar** , invoca a caixa de diálogo **Com disco** e especifica o caminho para o programa.</span><span class="sxs-lookup"><span data-stu-id="3298a-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="3298a-121">O painel de controle executa o programa e chama a função de ponto de entrada do seu serviço de mensagem com o parâmetro _ulContext_ definido como MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="3298a-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="3298a-122">Como os perfis são uma parte descartáveis da arquitetura do MAPI, certifique-se de que seu programa de instalação não armazene nada no perfil padrão que seria difícil de recriar.</span><span class="sxs-lookup"><span data-stu-id="3298a-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="3298a-123">Não há nenhuma utilitários para recuperação de perfil, para mover os perfis de um computador para outro, para backup off-line ou para restauração individual ou global de cópias de backup.</span><span class="sxs-lookup"><span data-stu-id="3298a-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3298a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3298a-124">See also</span></span>



[<span data-ttu-id="3298a-125">Implementação do serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="3298a-125">Message Service Implementation</span></span>](message-service-implementation.md)

