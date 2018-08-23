---
title: Repositórios de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576908"
---
# <a name="default-message-stores"></a>Repositórios de mensagens padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um armazenamento de mensagens padrão é aquela que aplicativos cliente podem usar para tarefas de mensagens de finalidade geral. Há um número de recursos opcionais para provedores de armazenamento de mensagem que se tornam necessários se o provedor de armazenamento de mensagem deve ser usado como o armazenamento de mensagens padrão. Eles são os seguintes:
  
- Implementando pastas especiais: as pastas de caixa de entrada, caixa de saída e os resultados da pesquisa.
    
- Fornecimento de relatórios de leitura e nonread.
    
- Permitindo que envios de mensagem de entrada e saída.
    
- Permitindo a criação de mensagens com classes de mensagens arbitrário.
    
- Dando suporte a propriedades nomeadas e de valores múltiplos.
    
- Suporte ao método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) , mesmo se o provedor de armazenamento de mensagem está firmemente combinado com um provedor de transporte. 
    
- Tabelas de conteúdo associado de suporte. Para obter mais informações, consulte [As tabelas de conteúdo](contents-tables.md).
    
- Dando suporte a notificação do spooler MAPI quando há mensagens na fila de mensagens de saída.
    
## <a name="see-also"></a>Confira também



[Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

