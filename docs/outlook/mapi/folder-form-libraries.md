---
title: Bibliotecas de formulários de pastas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580548"
---
# <a name="folder-form-libraries"></a>Bibliotecas de formulários de pastas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em alguns casos, talvez você queira associar um ou mais formulários uma pasta específica. Por exemplo, os funcionários em sua organização poderia ter uma pasta do relatório de andamento no seu armazenamento de mensagens pessoais para criação de relatórios de progresso de armazenamento. Como o relatório de andamento é específico para a pasta do relatório de andamento de cada usuário, ele pode não ser apropriado armazenar o formulário de relatório de progresso na biblioteca do formulário de todo o sistema. No entanto, uma cópia do formulário de relatório de andamento pode ser mantida na tabela associados de conteúdo da pasta do relatório de andamento de cada usuário. Isso impede que o usuário usando os formulários de relatório de andamento fora da pasta designada.
  
Conceitualmente, há uma biblioteca de formulários de pasta para todas as pastas em um armazenamento de mensagens, mesmo se não há servidores de formulário são instalados nela. Bibliotecas de formulários pasta são implementadas como outras bibliotecas de formulários — eles são armazenados como tabelas de conteúdo associado na parte alternativo da pasta. Como as bibliotecas de formulários pasta estão contidas na pasta, eles são copiados juntamente com sua pasta pai nas operações de cópia.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

