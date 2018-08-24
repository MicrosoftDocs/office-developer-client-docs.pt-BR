---
title: Visão geral dos formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1b3afeaa-4ede-41eb-a3c1-b8947a46ef97
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29132f24547dc744efcd6f2b6e4a8f6af87ab53c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574409"
---
# <a name="mapi-forms-overview"></a>Visão geral dos formulários MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador de uma mensagem. Cada mensagem tem uma classe de mensagem que dita o determinado formulário que é usado como seu visualizador. MAPI define várias classes de mensagem e implementou os formulários para exibir mensagens dessas classes. Os desenvolvedores de software cliente podem criar novas classes de mensagem e formulários personalizados para exibir mensagens criadas usando-se as novas classes.
  
Cada formulário personalizado implementa um conjunto de comandos de menu padrão, **Abrir**, **criar**, **Excluir**e **responder**e um conjunto de comandos que são específicos para o formulário específico. Alguns dos comandos de formulário são integrados com a interface do usuário do aplicativo cliente quando o formulário estiver ativo; outros comandos de formulário substituem completamente os comandos do cliente. 
  
A ilustração a seguir mostra a relação entre os componentes MAPI envolvidos no uso de formulários. 
  
**MAPI form architecture**
  
![Arquitetura de formulário MAPI] (media/forms01.gif "Arquitetura de formulário MAPI")
  
No diagrama, observe que o Gerenciador de formulário desempenha um papel que é semelhante a outros provedores de serviço MAPI, embora não seja um provedor de serviço em si. O Gerenciador de formulário é uma DLL substituível que implementa algumas das interfaces de MAPI. Embora os desenvolvedores podem implementar sua próprias Gerenciador de formulário, a maioria dos ambientes usará o Gerenciador de formulário fornecido pela Microsoft devido à complexidade do gerente do formulário.
  
A lista a seguir descreve os componentes no diagrama e sua relação com outros componentes:
  
- Cliente de mensagens: um aplicativo que pode usar os objetos de formulário. O cliente de mensagens usa as interfaces de formulário MAPI para se comunicar com o Gerenciador de formulário para carregar as mensagens em objetos de formulário.
    
- Interfaces de formulário MAPI: um padrão definido para a comunicação entre os componentes MAPI que estão relacionados a formulários.
    
- Gerenciador de formulário: DLL usado por clientes de mensagens para lidar com a instalação de formulários em bibliotecas de formulários, carregamento de servidores de formulário e comunicação inicial entre clientes de mensagens e os servidores do formulário.
    
- Bibliotecas de formulários: armazenamento permanente para os arquivos executáveis associados aos servidores de formulário.
    
- Servidores de formulário: arquivos executáveis que implementam um formulário. Servidores de formulário criam objetos de formulário e interfaces do usuário para lidar com mensagens específicas. Este executável também é um servidor OLE e de acordo com as convenções OLE usuais.
    
- Objetos de formulário: criados pelos servidores de formulário que correspondem às mensagens específicas de objetos de tempo de execução. Objetos de formulário são executados no mesmo contexto de processo como seu servidor de formulário.
    
Para obter mais informações sobre os componentes de formulário MAPI, consulte [Formulários MAPI](mapi-forms.md).
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

