---
title: Instâncias de disco e tabelas de cache
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d556ff4d-e2f3-4c83-a93f-b1bfda5abc8c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4f0b66476b1ab3d149b6f7e7b8171de7a509b597
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436752"
---
# <a name="disk-instances-and-cache-tables"></a>Instâncias de disco e tabelas de cache

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para ativar um formulário, seus arquivos executáveis devem estar disponíveis no computador do usuário. Se não estão disponíveis, devem ser copiados da biblioteca de formulário para o disco local. Para fazer isso, o gerenciador de formulário padrão cria um subdiretório no diretório do Windows do usuário para conter os arquivos executáveis do formulário (. EXEs,. HLPs). Esse diretório é conhecido como a instância de disco do formulário.
  
O gerenciador de formulário padrão mantém uma tabela de todas as instâncias de disco para que, se uma instância de disco já existir, ela possa ser usada sem precisar copiar arquivos da biblioteca de formulário para o disco do usuário. A tabela de instâncias de disco é gerenciada como um cache usado com menos frequência. Se uma nova instância de disco for necessária, ela será copiada para o computador do usuário, substituindo a instância de disco usada com menos frequência. A tabela de cache da instância de disco é atualizada para refletir a configuração mais recente. O tamanho do cache de disco é uma opção configurável pelo usuário, permitindo que os usuários equilibrem a velocidade com a capacidade de disco disponível.
  
Além do cache da instância de disco, o gerenciador de formulário padrão mantém uma tabela de instância em execução que lista todas as instâncias em execução de servidores de formulário no computador do usuário. Isso usa a capacidade de MAPI para manter instâncias de formulário ociosas em execução em um estado invisível até que uma forma da classe de mensagens desse servidor de formulário seja ativado. Em outras palavras, os servidores de formulário podem ser armazenados em cache na RAM para minimizar o número de vezes que o executável de um formulário deve estar localizado em uma biblioteca de formulário e carregado na memória do disco ou pela rede. Assim como o cache da instância de disco, o cache de instância em execução se comporta de forma menos usada para que uma instância de formulário em execução possa ser limpa do cache para dar espaço a outra instância de formulário. Esse cache é pesquisado por uma instância em execução de um servidor de formulário antes que as bibliotecas de formulário sejam pesquisadas para o servidor de formulário.
  
> [!NOTE]
> O gerenciador de formulário padrão exibe um indicador de progresso ao instalar um formulário na estação de trabalho de um usuário, permitindo que o usuário cancele a operação. Isso será especialmente útil se a conexão do usuário com o arquivo executável do servidor de formulário estiver em uma rede de baixa largura de banda. 
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

