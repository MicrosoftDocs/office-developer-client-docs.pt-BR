---
title: Visão geral de formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4e7d48f6f6a47ce28aa0e1291ccef209b998c18e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351509"
---
# <a name="mapi-forms-overview"></a>Visão geral de formulários MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador de uma mensagem. Cada mensagem tem uma classe de mensagem que determina o formulário específico que é usado como seu visualizador. O MAPI define várias classes de mensagens e implementou os formulários para exibir mensagens dessas classes. Os desenvolvedores de software cliente podem criar novas classes de mensagens e formulários personalizados para exibir mensagens criadas usando as novas classes.
  
Todos os formulários personalizados implementam um conjunto de comandos de menu padrão, como **abrir**, **criar**, **excluir**e **responder**e um conjunto de comandos específicos para o formulário específico. Alguns dos comandos de formulário estão integrados à interface do usuário do aplicativo cliente quando o formulário está ativo; outros comandos de formulário substituem completamente os comandos do cliente. 
  
A ilustração a seguir mostra a relação entre os componentes MAPI envolvidos no uso de formulários. 
  
**MAPI form architecture**
  
![Arquitetura de formulários MAPI] (media/forms01.gif "Arquitetura de formulários MAPI")
  
No diagrama, observe que o gerente de formulário desempenha uma função semelhante a outros provedores de serviço MAPI, embora não seja um provedor de serviços propriamente dito. O Gerenciador de formulários é uma DLL substituível que implementa algumas das interfaces MAPI. Embora os desenvolvedores possam implementar seus próprios gerentes de formulário, a maioria dos ambientes usará o Gerenciador de formulários fornecido pela Microsoft devido à complexidade do gerente de formulários.
  
A lista a seguir descreve os componentes no diagrama e sua relação com outros componentes:
  
- Cliente de mensagens: um aplicativo que pode usar objetos Form. O cliente de mensagens usa as interfaces de formulário MAPI para se comunicar com o Gerenciador de formulários para carregar mensagens em objetos de formulário.
    
- Interfaces de formulário MAPI: um padrão definido para comunicação entre componentes MAPI relacionados a formulários.
    
- Gerenciador de formulários: a DLL que os clientes de mensagens usam para lidar com a instalação de formulários em bibliotecas de formulários, carregamento de servidores de formulários e comunicação inicial entre clientes de mensagens e servidores de formulário.
    
- Bibliotecas de formulários: armazenamento permanente para os arquivos executáveis associados aos servidores de formulários.
    
- Servidores de formulário: arquivos executáveis que implementam um formulário. Os servidores de formulário criam objetos de formulário e interfaces de usuário para lidar com mensagens específicas. Esse executável também é um servidor OLE e obedece às convenções de OLE usuais.
    
- Objetos Form: objetos de tempo de execução criados por servidores de formulário que correspondem a mensagens específicas. Os objetos Form são executados no mesmo contexto de processo que seu servidor de formulário.
    
Para obter mais informações sobre os componentes de formulário MAPI, consulte [MAPI Forms](mapi-forms.md).
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

