---
title: Repositórios de mensagem padrão
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766363"
---
# <a name="default-message-stores"></a>Repositórios de mensagem padrão

  
  
**Aplica-se a**: Outlook 
  
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



[Desenvolvendo um provedor de armazenamento de mensagens MAPI](developing-a-mapi-message-store-provider.md)

