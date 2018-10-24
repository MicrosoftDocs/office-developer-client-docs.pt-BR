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
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580548"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="1a75b-103">Bibliotecas de formulários de pastas</span><span class="sxs-lookup"><span data-stu-id="1a75b-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="1a75b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a75b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a75b-105">Em alguns casos, talvez você queira associar um ou mais formulários uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="1a75b-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="1a75b-106">Por exemplo, os funcionários em sua organização poderia ter uma pasta do relatório de andamento no seu armazenamento de mensagens pessoais para criação de relatórios de progresso de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1a75b-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="1a75b-107">Como o relatório de andamento é específico para a pasta do relatório de andamento de cada usuário, ele pode não ser apropriado armazenar o formulário de relatório de progresso na biblioteca do formulário de todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="1a75b-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="1a75b-108">No entanto, uma cópia do formulário de relatório de andamento pode ser mantida na tabela associados de conteúdo da pasta do relatório de andamento de cada usuário.</span><span class="sxs-lookup"><span data-stu-id="1a75b-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="1a75b-109">Isso impede que o usuário usando os formulários de relatório de andamento fora da pasta designada.</span><span class="sxs-lookup"><span data-stu-id="1a75b-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="1a75b-110">Conceitualmente, há uma biblioteca de formulários de pasta para todas as pastas em um armazenamento de mensagens, mesmo se não há servidores de formulário são instalados nela.</span><span class="sxs-lookup"><span data-stu-id="1a75b-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="1a75b-111">Bibliotecas de formulários pasta são implementadas como outras bibliotecas de formulários — eles são armazenados como tabelas de conteúdo associado na parte alternativo da pasta.</span><span class="sxs-lookup"><span data-stu-id="1a75b-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="1a75b-112">Como as bibliotecas de formulários pasta estão contidas na pasta, eles são copiados juntamente com sua pasta pai nas operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="1a75b-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1a75b-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a75b-113">See also</span></span>



[<span data-ttu-id="1a75b-114">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="1a75b-114">MAPI Forms</span></span>](mapi-forms.md)

