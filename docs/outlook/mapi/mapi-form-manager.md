---
title: Gerenciador de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0bbbd06-d47d-45ad-8179-2372d1d023d0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d12d879ea5a82c5e0e3978d90694b3851aaac5cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767852"
---
# <a name="mapi-form-manager"></a>Gerenciador de formulário MAPI

  
  
**Aplica-se a**: Outlook 
  
Um gerente de formulário é um objeto que implementa a interface [IMAPIFormMgr](imapiformmgriunknown.md) . A maioria das organizações usará o Gerenciador de formulário fornecido com MAPI, conhecido como o Gerenciador de formulário padrão. No entanto, uma organização pode substituir o Gerenciador de formulário padrão por um gerente de formulário personalizado, se desejado. O gerente do formulário cuida de localizar os formulários dentro de bibliotecas de formulários, carregando formulários em resposta às solicitações dos usuários e instalando formulários para a biblioteca de formulários particulares, biblioteca de formulários de pasta ou biblioteca de formulários local para um usuário. 
  
Para um usuário interagir com uma mensagem, uma instância do servidor de formulário para a classe de mensagem da mensagem deve ser criada e ativada para exibir a mensagem e realizar a operação solicitada na mensagem. Conforme descrito no tópico [MAPI bibliotecas de formulários](mapi-form-libraries.md), a implementação de um formulário pode existir em vários locais diferentes (bibliotecas de formulários) e não há nenhuma garantia de que um formulário ou o seu servidor será disponível localmente ou em uma execução de estado quando um usuário deseja interagir com ele. O gerente do formulário cuida dos detalhes de localização e ativando o formulário.
  
Clientes usam os serviços fornecidos pelo gerente de formulário para localizar e ativar formulários. A interface **IMAPIFormMgr** é implementada pelo gerente de formulário e é chamada pelos clientes para acessar seus serviços. O Gerenciador de formulário é um componente essencial porque ele oculta quase todos os detalhes de localização e ativando formulários de clientes de mensagem. 
  
Ao carregar os servidores de formulário, o gerente do formulário padrão carrega o formulário da biblioteca de formulários primeira em que se encontra uma implementação para a classe de mensagem do formulário. O Gerenciador de formulário padrão pesquisará as bibliotecas de formulários na seguinte ordem:
  
1. Biblioteca de formulários locais do usuário. Esta biblioteca de formulários é pesquisada primeiro porque ele fornece o acesso mais rápido a implementação de um formulário, se a implementação estiver instalada na biblioteca de formulários local.
    
2. A biblioteca de formulários de pasta do contêiner da mensagem — a pasta na qual a mensagem está sendo carregada é armazenada.
    
3. Biblioteca de formulários particular do usuário.
    
Um gerente de formulário personalizado pode pesquisar as bibliotecas de formulário disponível em qualquer ordem, ou pode implementar outras bibliotecas de formulários, como uma biblioteca de formulários de toda a organização. Para obter mais detalhes sobre as bibliotecas de formulários, consulte [Bibliotecas de formulários de MAPI](mapi-form-libraries.md). 
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

