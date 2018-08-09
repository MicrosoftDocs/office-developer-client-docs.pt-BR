---
title: Manter uma biblioteca de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767784"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="6b2c3-103">Manter uma biblioteca de formulários</span><span class="sxs-lookup"><span data-stu-id="6b2c3-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="6b2c3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b2c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b2c3-105">Uma biblioteca de formulários contém todas as informações importantes sobre um formulário: arquivos executáveis do seu servidor, seus verbos e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="6b2c3-106">Alguns clientes permitir que seus usuários a manter, instalar ou remover servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="6b2c3-107">Se você deseja oferecer esse recurso para seus usuários, você deve ter acesso ao:</span><span class="sxs-lookup"><span data-stu-id="6b2c3-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="6b2c3-108">Arquivo de configuração do servidor de formulário, um arquivo com o. Extensão de configuração.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="6b2c3-109">Objeto de contêiner da biblioteca de formulários, um objeto que implementa o [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="6b2c3-110">Para acessar o arquivo de configuração ou um nome de caminho a ela, use qualquer meio é conveniente.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="6b2c3-111">Geralmente, os clientes apresentam ao usuário com uma caixa de diálogo de instalação e remoção de servidores de formulário que também podem ser usados para avisar o usuário para o local do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="6b2c3-112">Para acessar o contêiner da biblioteca de formulários, chame o método de [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) do gerente do formulário.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="6b2c3-113">Passe um valor de enumeração para especificar qual biblioteca de formulários para abrir e se necessário, um ponteiro para o objeto que o gerente do formulário deve usar para abrir a biblioteca de formulários.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="6b2c3-114">Por exemplo, se você está abrindo uma [Pasta bibliotecas de formulários](folder-form-libraries.md), passe uma [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="6b2c3-115">Após **OpenFormContainer** retorna o ponteiro **IMAPIFormContainer** , chame Update [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) ou [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), dependendo de manutenção a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="6b2c3-116">**InstallForm** adiciona um servidor de formulário para a biblioteca; **RemoveForm** exclui um servidor de formulário da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6b2c3-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  
