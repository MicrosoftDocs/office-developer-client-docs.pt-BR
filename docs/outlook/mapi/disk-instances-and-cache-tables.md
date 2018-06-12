---
title: Instâncias de disco e tabelas de Cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c3b371a226c9eb6a3cf675ee316bf22a597fe806
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766418"
---
# <a name="disk-instances-and-cache-tables"></a>Instâncias de disco e tabelas de Cache

**Aplica-se a**: Outlook 
  
Para ativar um formulário, seus arquivos executáveis devem estar disponíveis no computador do usuário. Se elas não estiverem disponíveis, eles devem ser copiados da biblioteca de formulários para o disco local. Para fazer isso, o gerente do formulário padrão cria um subdiretório no diretório do Windows do usuário para contêm arquivos executáveis do formulário (. Executáveis. HLPs). Esse diretório é conhecido como a instância do disco do formulário.
  
O Gerenciador de formulário padrão mantém uma tabela de todas as instâncias de disco para que se já existir uma instância de disco pode ser usado sem precisar copiar os arquivos da biblioteca de formulários para o disco do usuário. A tabela de instâncias de disco é gerenciada como um cache menos frequentemente utilizado. Se for necessária uma nova instância do disco, ele é copiado para o computador do usuário, substituindo a instância do disco menos frequentemente utilizado. A tabela de cache de instância do disco, em seguida, é atualizada para refletir a configuração mais recente. O tamanho do cache de disco é uma opção configurável pelo usuário, permitindo que os usuários equilibrar velocidade com capacidade em disco disponível.
  
Além do cache de instância do disco, o gerente do formulário padrão mantém uma tabela de instância em execução que lista todas as instâncias em execução dos servidores de formulário no computador do usuário. Usa a capacidade do MAPI para manter as instâncias de formulário ocioso em execução em um estado invisível até que a mensagem do servidor é ativado a classe de formulário de um formulário do que. Em outras palavras, servidores de formulário podem ser armazenados em cache na RAM para minimizar o número de vezes executável de um formulário deve ser localizado dentro de uma biblioteca de formulários e carregado na memória do disco ou pela rede. Como o cache de instância do disco, o cache de instância em execução se comporta de maneira menores usados para que uma instância de formulário em execução pode ser removida do cache para liberar espaço para outra instância do formulário. Este cache é pesquisado para uma instância de um servidor de formulário em execução antes que as bibliotecas de formulário são pesquisadas para o servidor do formulário.
  
> [!NOTE]
> O Gerenciador de formulário padrão exibe um indicador de progresso quando a instalação de um formulário na estação de trabalho do usuário, permitindo que o usuário cancelar a operação. Isso é especialmente útil se a conexão do usuário para o arquivo executável do servidor formulário estiver em uma rede de baixa largura de banda. 
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

