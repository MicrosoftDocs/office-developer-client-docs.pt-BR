---
title: Gerenciador de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3059183103ca2552505486b5ec54366729ae4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430193"
---
# <a name="mapi-form-manager"></a>Gerenciador de formulários MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um gerente de formulários é um objeto que implementa a interface [IMAPIFormMgr](imapiformmgriunknown.md) . A maioria das organizações usará o Gerenciador de formulários fornecido com MAPI, chamado de Gerenciador de formulários padrão. No enTanto, uma organização pode substituir o Gerenciador de formulários padrão por um gerente de formulário personalizado, se desejado. O gerente de formulários cuida da localização de formulários nas bibliotecas de formulários, carregando formulários em resposta às solicitações do usuário e instalando formulários na biblioteca de formulários local, na biblioteca de formulários de pastas ou na biblioteca de formulários pessoais de um usuário. 
  
Para que um usuário interaja com uma mensagem, uma instância do servidor de formulário da classe Message da mensagem deve ser criada e ativada para exibir a mensagem e realizar a operação solicitada na mensagem. Conforme descrito no tópico [bibliotecas de formulários MAPI](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulários) e não há garantia de que um formulário ou seu servidor estará localmente disponível ou em um estado de execução quando um usuário quiser interagir com ele. O gerente de formulários cuida dos detalhes da localização e ativação do formulário.
  
Os clientes usam os serviços fornecidos pelo gerente de formulários para localizar e ativar formulários. A interface **IMAPIFormMgr** é implementada pelo Gerenciador de formulários e é chamada por clientes para acessar seus serviços. O Gerenciador de formulários é um componente essencial porque oculta quase todos os detalhes de encontrar e ativar formulários de clientes de mensagens. 
  
Ao carregar servidores de formulário, o Gerenciador de formulários padrão carrega o formulário a partir da primeira biblioteca de formulários na qual uma implementação da classe de mensagem do formulário é encontrada. O Gerenciador de formulários padrão pesquisa as bibliotecas de formulários na seguinte ordem:
  
1. A biblioteca de formulários local do usuário. Esta biblioteca de formulários é pesquisada primeiro porque fornece o acesso mais rápido à implementação de um formulário se a implementação estiver instalada na biblioteca de formulários local.
    
2. A biblioteca de formulários de pasta do contêiner da mensagem — a pasta na qual a mensagem que está sendo carregada está armazenada.
    
3. A biblioteca de formulários pessoais do usuário.
    
Um gerente de formulário personalizado pode pesquisar as bibliotecas de formulários disponíveis em qualquer ordem, ou pode implementar outras bibliotecas de formulários, como uma biblioteca de formulários em toda a organização. Para obter mais detalhes sobre bibliotecas de formulários, consulte [bibliotecas de formulários MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

