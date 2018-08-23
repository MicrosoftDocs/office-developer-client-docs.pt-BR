---
title: Instalar um formulário em uma biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d3b20c9fb4b4f1a26eb4ed1a9a498bd56a915a70
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579778"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="269d9-103">Instalar um formulário em uma biblioteca</span><span class="sxs-lookup"><span data-stu-id="269d9-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="269d9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="269d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="269d9-105">O Gerenciador de formulário MAPI padrão fornecido com o SDK do Windows não fornece uma interface de usuário de instalação formulários nas várias bibliotecas de formulário.</span><span class="sxs-lookup"><span data-stu-id="269d9-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="269d9-106">Dessa forma, você precisará criar um aplicativo pequeno — ou detalhados de conjunto de instruções — que os usuários podem usar para instalar o formulário.</span><span class="sxs-lookup"><span data-stu-id="269d9-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="269d9-107">Se você implementar um aplicativo de instalação, a série de ações ele deve executar para instalar um formulário em associado conteúdo de uma pasta tabela são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="269d9-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="269d9-108">Chame a função de [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir o formulário manager.</span><span class="sxs-lookup"><span data-stu-id="269d9-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="269d9-109">Use o método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) ou [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para selecionar e abrir o contêiner de destino para o formulário.</span><span class="sxs-lookup"><span data-stu-id="269d9-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="269d9-110">Use a função [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar o formulário.</span><span class="sxs-lookup"><span data-stu-id="269d9-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="269d9-111">As etapas 4 a 6 são para instalação em uma biblioteca de formulários local:</span><span class="sxs-lookup"><span data-stu-id="269d9-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="269d9-112">Copie todos os arquivos para o local apropriado no disco local, se a instalação é a biblioteca de formulários local na estação de trabalho do usuário.</span><span class="sxs-lookup"><span data-stu-id="269d9-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="269d9-113">Se necessário, modifique o arquivo de configuração de formulário para refletir o atuais caminhos dos componentes.</span><span class="sxs-lookup"><span data-stu-id="269d9-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="269d9-114">O arquivo de configuração de formulário pode conter caminhos relativos, caso em que esta etapa talvez não seja necessária.</span><span class="sxs-lookup"><span data-stu-id="269d9-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="269d9-115">Conclua as etapas apropriadas de registro OLE para associar o tipo de mensagem com o servidor de formulário que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="269d9-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="269d9-116">Se o formulário foi instalado na biblioteca de formulários local, copie o ícone (. ico) do formulário e arquivos de configuração (. cfg) no diretório %WINDOWS%\FORMS\CONFIGS para que o formulário possa ser restaurado automaticamente caso a biblioteca de formulários está corrompida ou excluída.</span><span class="sxs-lookup"><span data-stu-id="269d9-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="269d9-117">Esta etapa é recomendado, mas não seja obrigatório.</span><span class="sxs-lookup"><span data-stu-id="269d9-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="269d9-118">Você pode simplificar a instalação em uma biblioteca de formulários locais, substituindo as etapas 1 e 2 por uma chamada para a função [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="269d9-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="269d9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="269d9-119">See also</span></span>



[<span data-ttu-id="269d9-120">Desenvolver servidores de formulário MAPI</span><span class="sxs-lookup"><span data-stu-id="269d9-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

