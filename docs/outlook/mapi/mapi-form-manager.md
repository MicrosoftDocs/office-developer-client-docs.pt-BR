---
title: MAPI Form Manager
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
# <a name="mapi-form-manager"></a>MAPI Form Manager

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um gerenciador de formulário é um objeto que implementa a interface [IMAPIFormMgr.](imapiformmgriunknown.md) A maioria das organizações usará o gerenciador de formulário fornecido com MAPI, conhecido como gerenciador de formulário padrão. No entanto, uma organização pode substituir o gerenciador de formulário padrão por um gerenciador de formulário personalizado, se desejado. O gerenciador de formulários cuida da localização de formulários em bibliotecas de formulários, do carregamento de formulários em resposta às solicitações do usuário e da instalação de formulários na biblioteca de formulários local do usuário, na biblioteca de formulários de pasta ou na biblioteca de formulários pessoais. 
  
Para que um usuário interaja com uma mensagem, uma instância do servidor de formulário para a classe de mensagem da mensagem deve ser criada e ativada para exibir a mensagem e executar a operação solicitada na mensagem. Conforme descrito no tópico [MapI Form Libraries](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulário) e não há garantia de que um formulário ou seu servidor estará disponível localmente ou em um estado de execução quando um usuário quiser interagir com ele. O gerenciador de formulário cuida dos detalhes de localizar e ativar o formulário.
  
Os clientes usam serviços fornecidos pelo gerenciador de formulários para encontrar e ativar formulários. A interface **IMAPIFormMgr** é implementada pelo gerenciador de formulário e é chamada pelos clientes para acessar seus serviços. O gerenciador de formulários é um componente essencial porque oculta quase todos os detalhes de localizar e ativar formulários de clientes de mensagens. 
  
When loading form servers, the default form manager loads the form from the first form library in which an implementation for the form's message class is found. O gerenciador de formulário padrão pesquisa as bibliotecas de formulário na seguinte ordem:
  
1. A biblioteca de formulário local do usuário. Essa biblioteca de formulário é pesquisada primeiro porque fornece o acesso mais rápido à implementação de um formulário se a implementação estiver instalada na biblioteca de formulário local.
    
2. A biblioteca de formulário de pasta do contêiner da mensagem — a pasta na qual a mensagem que está sendo carregada é armazenada.
    
3. A biblioteca de formulário pessoal do usuário.
    
Um gerenciador de formulário personalizado pode pesquisar as bibliotecas de formulário disponíveis em qualquer ordem ou pode implementar outras bibliotecas de formulário, como uma biblioteca de formulário em toda a organização. Para obter mais detalhes sobre bibliotecas de formulário, consulte [MAPI Form Libraries](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

