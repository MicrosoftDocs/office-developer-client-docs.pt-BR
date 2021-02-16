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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416535"
---
# <a name="handling-a-transport-provider"></a>Manipular um provedor de transporte
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes se comunicam com provedores de transporte por meio de objetos de status fornecidos por provedores de transporte e o spooler MAPI. Os clientes acessam objetos de status [chamando IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar a tabela de status. Os objetos de status implementam a interface [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) que tem métodos para configurar provedores, liberar filas de mensagens de entrada e saída, definir senhas e validação de estado. Para obter mais informações sobre objetos de status, consulte [Status Table and Status Objects](status-table-and-status-objects.md).


- [Enviar ou receber uma mensagem sob demanda:](sending-or-receiving-a-message-on-demand.md)descreve como enviar ou receber uma mensagem sob demanda.
    
- [Setting Transport Order](setting-transport-order.md): Describes how to set transport order.
    
- [Reconfigurando um Provedor de Transporte:](reconfiguring-a-transport-provider.md)descreve como reconfigurar um provedor de transporte e quais propriedades estão disponíveis para definir.
    

