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
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567948"
---
# <a name="handling-a-transport-provider"></a>Manipular um provedor de transporte
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes se comuniquem com provedores de transporte por meio de objetos de status fornecidos por provedores de transporte e o spooler MAPI. Clientes acessam objetos de status chamando [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar a tabela de status. Objetos de status implementar o [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) interface, que tem métodos para configurando provedores, liberação de entrada e saída da mensagem filas, senhas de configuração e validação de estado. Para obter mais informações sobre objetos de status, consulte a [tabela de Status e objetos de Status](status-table-and-status-objects.md).


- [Enviar ou receber uma mensagem sob demanda](sending-or-receiving-a-message-on-demand.md): descreve como enviar ou receber uma mensagem sob demanda.
    
- [Ordem de transporte de configuração](setting-transport-order.md): descreve como definir a ordem de transporte.
    
- [Reconfiguração de um provedor de transporte](reconfiguring-a-transport-provider.md): descreve como reconfigurar um provedor de transporte e as propriedades que estão disponíveis para definir.
    

