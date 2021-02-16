---
title: Bibliotecas de Formulário de Pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414281"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="ffa8e-103">Bibliotecas de Formulário de Pasta</span><span class="sxs-lookup"><span data-stu-id="ffa8e-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="ffa8e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffa8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffa8e-105">Em alguns casos, talvez você queira associar um ou mais formulários a uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="ffa8e-106">Por exemplo, os funcionários em sua organização podem ter uma pasta do Relatório de Progresso em seu armazenamento de mensagens pessoais para criar e armazenar relatórios de progresso.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="ffa8e-107">Como o relatório de progresso é específico para a pasta Relatório de Progresso de cada usuário, talvez não seja apropriado armazenar o formulário de relatório de progresso na biblioteca de formulário em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="ffa8e-108">No entanto, uma cópia do formulário de relatório de progresso pode ser mantida na tabela de conteúdo associado da pasta Relatório de Progresso de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="ffa8e-109">Isso restringe o usuário de usar formulários de relatório de progresso fora da pasta designada.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="ffa8e-110">Conceitualmente, há uma biblioteca de formulário de pasta para cada pasta em um armazenamento de mensagens, mesmo se nenhum servidor de formulário estiver instalado nele.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="ffa8e-111">As bibliotecas de formulário de pasta são implementadas como outras bibliotecas de formulário — elas são armazenadas como tabelas de conteúdo associadas na parte alternativa da pasta.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="ffa8e-112">Como as bibliotecas de formulário de pasta estão contidas na pasta, elas são copiadas junto com sua pasta pai nas operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="ffa8e-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ffa8e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffa8e-113">See also</span></span>



[<span data-ttu-id="ffa8e-114">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="ffa8e-114">MAPI Forms</span></span>](mapi-forms.md)

