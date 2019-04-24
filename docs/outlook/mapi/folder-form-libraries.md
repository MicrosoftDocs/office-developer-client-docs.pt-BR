---
title: Bibliotecas de formulários de pastas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281554"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="d9c96-103">Bibliotecas de formulários de pastas</span><span class="sxs-lookup"><span data-stu-id="d9c96-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="d9c96-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9c96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9c96-105">Em alguns casos, talvez você queira associar um ou mais formulários a uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="d9c96-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="d9c96-106">Por exemplo, os funcionários de sua organização podem ter uma pasta de relatórios de progresso no repositório de mensagens pessoais para criar e armazenar relatórios de progresso.</span><span class="sxs-lookup"><span data-stu-id="d9c96-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="d9c96-107">Como o relatório de progresso é específico para a pasta de relatórios de progresso de cada usuário, talvez não seja apropriado armazenar o formulário de relatório de progresso na biblioteca de formulários de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="d9c96-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="d9c96-108">No enTanto, uma cópia do formulário de relatório de progresso pode ser mantida na tabela de conteúdo associado da pasta de relatório de progresso de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="d9c96-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="d9c96-109">Isso restringe o usuário de usar formulários de relatório de progresso fora da pasta designada.</span><span class="sxs-lookup"><span data-stu-id="d9c96-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="d9c96-110">Conceitualmente, há uma biblioteca de formulários de pasta para cada pasta em um repositório de mensagens, mesmo se nenhum servidor de formulário estiver instalado nele.</span><span class="sxs-lookup"><span data-stu-id="d9c96-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="d9c96-111">Bibliotecas de formulários de pasta são implementadas como outras bibliotecas de formulários, elas são armazenadas como tabelas de conteúdo associado na parte alternativa da pasta.</span><span class="sxs-lookup"><span data-stu-id="d9c96-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="d9c96-112">Como as bibliotecas de formulários de pastas estão contidas na pasta, elas são copiadas junto com a pasta pai em operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="d9c96-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9c96-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9c96-113">See also</span></span>



[<span data-ttu-id="d9c96-114">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="d9c96-114">MAPI Forms</span></span>](mapi-forms.md)

