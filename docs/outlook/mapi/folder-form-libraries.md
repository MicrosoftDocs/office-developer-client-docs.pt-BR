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
# <a name="folder-form-libraries"></a>Bibliotecas de Formulário de Pasta

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em alguns casos, talvez você queira associar um ou mais formulários a uma pasta específica. Por exemplo, os funcionários em sua organização podem ter uma pasta do Relatório de Progresso em seu armazenamento de mensagens pessoais para criar e armazenar relatórios de progresso. Como o relatório de progresso é específico para a pasta Relatório de Progresso de cada usuário, talvez não seja apropriado armazenar o formulário de relatório de progresso na biblioteca de formulário em todo o sistema. No entanto, uma cópia do formulário de relatório de progresso pode ser mantida na tabela de conteúdo associado da pasta Relatório de Progresso de cada usuário. Isso restringe o usuário de usar formulários de relatório de progresso fora da pasta designada.
  
Conceitualmente, há uma biblioteca de formulário de pasta para cada pasta em um armazenamento de mensagens, mesmo se nenhum servidor de formulário estiver instalado nele. As bibliotecas de formulário de pasta são implementadas como outras bibliotecas de formulário — elas são armazenadas como tabelas de conteúdo associadas na parte alternativa da pasta. Como as bibliotecas de formulário de pasta estão contidas na pasta, elas são copiadas junto com sua pasta pai nas operações de cópia.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

