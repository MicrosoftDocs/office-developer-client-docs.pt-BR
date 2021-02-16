---
title: Instalando um formulário em uma biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433140"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="787db-103">Instalando um formulário em uma biblioteca</span><span class="sxs-lookup"><span data-stu-id="787db-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="787db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="787db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="787db-105">O gerenciador de formulários MAPI padrão fornecido com o SDK do Windows não fornece uma interface do usuário para instalar formulários nas várias bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="787db-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="787db-106">Por isso, você terá que criar um pequeno aplicativo — ou um conjunto detalhado de instruções — que os usuários podem usar para instalar o formulário.</span><span class="sxs-lookup"><span data-stu-id="787db-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="787db-107">Se você implementar um aplicativo de instalação, as séries de ações que ele deve executar para instalar um formulário em uma tabela de conteúdo associada de uma pasta são as seguinte:</span><span class="sxs-lookup"><span data-stu-id="787db-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="787db-108">Chame a [função MAPIOpenFormMgr](mapiopenformmgr.md) para abrir o gerenciador de formulário.</span><span class="sxs-lookup"><span data-stu-id="787db-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="787db-109">Use [o método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para selecionar e abrir o contêiner de destino do formulário.</span><span class="sxs-lookup"><span data-stu-id="787db-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="787db-110">Use a [função IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar o formulário.</span><span class="sxs-lookup"><span data-stu-id="787db-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="787db-111">As etapas 4 a 6 são para instalação em uma biblioteca de formulário local:</span><span class="sxs-lookup"><span data-stu-id="787db-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="787db-112">Copie todos os arquivos para o local apropriado no disco local, se a instalação for na biblioteca de formulário local na estação de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="787db-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="787db-113">Se necessário, modifique o arquivo de configuração do formulário para refletir os caminhos atuais dos componentes.</span><span class="sxs-lookup"><span data-stu-id="787db-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="787db-114">O arquivo de configuração do formulário pode conter caminhos relativos e, nesse caso, esta etapa pode não ser necessária.</span><span class="sxs-lookup"><span data-stu-id="787db-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="787db-115">Conclua as etapas de registro OLE apropriadas para associar o tipo de mensagem ao servidor de formulário que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="787db-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="787db-116">Se o formulário foi instalado na biblioteca de formulários local, copie o ícone do formulário (.ico) e os arquivos de configuração (.cfg) no diretório %WINDOWS%\FORMS\CONFIGS para que o formulário possa ser automaticamente restaurado caso a biblioteca de formulários seja corrompida ou excluída.</span><span class="sxs-lookup"><span data-stu-id="787db-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="787db-117">Esta etapa é recomendada, mas não obrigatória.</span><span class="sxs-lookup"><span data-stu-id="787db-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="787db-118">Você pode simplificar a instalação em uma biblioteca de formulário local substituindo as etapas 1 e 2 por uma chamada para a função [MAPIOpenLocalFormContainer.](mapiopenlocalformcontainer.md)</span><span class="sxs-lookup"><span data-stu-id="787db-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="787db-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="787db-119">See also</span></span>



[<span data-ttu-id="787db-120">Desenvolvendo servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="787db-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

