---
title: Manipular um provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299493"
---
# <a name="handling-a-transport-provider"></a>Manipular um provedor de transporte
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes se comunicam com provedores de transporte por meio de objetos de status fornecidos por provedores de transporte e pelo spooler MAPI. Os clientes acessam objetos de status chamando [IMAPISession::](imapisession-getstatustable.md) getstatustable para recuperar a tabela status. Os objetos de status implementam a interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) , que tem métodos para configurar provedores, liberar filas de mensagens de entrada e de saída, definir senhas e validação de estado. Para obter mais informações sobre objetos de status, consulte [tabela de status e objetos de status](status-table-and-status-objects.md).


- [Enviando ou recebendo uma mensagem sob demanda](sending-or-receiving-a-message-on-demand.md): descreve como enviar ou receber uma mensagem sob demanda.
    
- [Configuração da ordem de transporte](setting-transport-order.md): descreve como definir a ordem de transporte.
    
- [Reconfiguração de um provedor de transporte](reconfiguring-a-transport-provider.md): descreve como reconfigurar um provedor de transporte e quais propriedades estão disponíveis para definir.
    

