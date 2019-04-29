---
title: Mantendo uma biblioteca de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408800"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="72671-103">Mantendo uma biblioteca de formulários</span><span class="sxs-lookup"><span data-stu-id="72671-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="72671-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72671-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72671-105">Uma biblioteca de formulários contém todas as informações importantes sobre um formulário: suas propriedades, seus verbos e os arquivos executáveis do servidor.</span><span class="sxs-lookup"><span data-stu-id="72671-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="72671-106">Alguns clientes permitem que seus usuários mantenham, instalem ou removam servidores de formulários.</span><span class="sxs-lookup"><span data-stu-id="72671-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="72671-107">Se quiser oferecer esse recurso aos seus usuários, você deve ter acesso ao:</span><span class="sxs-lookup"><span data-stu-id="72671-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="72671-108">O arquivo de configuração do servidor de formulário, um arquivo com o. Extensão CFG.</span><span class="sxs-lookup"><span data-stu-id="72671-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="72671-109">O objeto contêiner da biblioteca de formulários, um objeto que implementa a interface [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="72671-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="72671-110">Para acessar o arquivo de configuração ou um nome de caminho para ele, use o que for conveniente.</span><span class="sxs-lookup"><span data-stu-id="72671-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="72671-111">Normalmente, os clientes apresentam ao usuário uma caixa de diálogo para instalar e remover servidores de formulários que também podem ser usados para solicitar ao usuário o local do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="72671-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="72671-112">Para acessar o contêiner da biblioteca de formulários, chame o método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) do gerente de formulários.</span><span class="sxs-lookup"><span data-stu-id="72671-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="72671-113">Passe um valor de enumeração para especificar qual biblioteca de formulários será aberta e, se necessário, um ponteiro para o objeto que o gerente de formulários deve usar para abrir a biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="72671-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="72671-114">Por exemplo, se você estiver abrindo uma [biblioteca de formulários de pasta](folder-form-libraries.md), passe um ponteiro de [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="72671-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="72671-115">Após **OpenFormContainer** retornar o ponteiro **IMAPIFormContainer** , chame [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md), dependendo da manutenção a ser executada.</span><span class="sxs-lookup"><span data-stu-id="72671-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="72671-116">**InstallForm** adiciona um servidor de formulários à biblioteca; **RemoveForm** exclui um servidor de formulários da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="72671-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

