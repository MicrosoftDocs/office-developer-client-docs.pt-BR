---
title: Repositórios de mensagens padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576908"
---
# <a name="default-message-stores"></a>Repositórios de mensagens padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um repositório de mensagens padrão é aquele que os aplicativos de clientes podem usar para tarefas de mensagens de finalidade geral. Há vários recursos opcionais de provedores de repositórios de mensagens que se tornam necessários se o provedor do repositório de mensagens precisar ser usado como repositório de mensagens padrão. São eles:
  
- Implementar as pastas especiais: as pastas de caixa de entrada e saída e de resultados de pesquisa.
    
- Fornecer relatórios de leitura e não leitura.
    
- Permitir envios de mensagens de entrada e saída.
    
- Permitir a criação de mensagens com classes de mensagem arbitrárias.
    
- Suportar propriedades nomeadas e de múltiplos valores.
    
- Suportar o método [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), mesmo que o provedor do repositório de mensagens esteja fortemente acoplado a um provedor de transporte. 
    
- Suportar tabelas de conteúdo associados. Para mais informações, confira [Tabelas de Conteúdo](contents-tables.md).
    
- Suporte à notificação do spooler MAPI quando há mensagens na fila de mensagens de saída.
    
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

