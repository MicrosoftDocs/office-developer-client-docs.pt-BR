---
title: Escolher uma classe de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285255"
---
# <a name="choosing-a-message-class"></a>Escolher uma classe de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conforme descrito em [classes de mensagens MAPI](mapi-message-classes.md), as classes de mensagem são importantes para o estabelecimento da relação entre tipos de mensagens personalizadas e, por extensão, entre os próprios servidores de formulário. Felizmente, a escolha de uma cadeia de caracteres de classe de mensagem é muito simples. A cadeia de caracteres de classe de mensagem de uma classe de mensagem é arbitrária, mas deve usar as seguintes convenções:
  
- A cadeia de caracteres deve satisfazer todas as convenções descritas na documentação da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Importante, a cadeia de caracteres deve ser composta totalmente de caracteres ANSI e ter menos de 256 caracteres.
    
- Se seu servidor de formulário é derivado de um servidor de formulário existente ou é uma extensão de um servidor de formulários existente, a cadeia de caracteres de classe da mensagem deve ser formada adicionando um ponto e outra palavra à cadeia de caracteres de classe de mensagem do servidor de formulário no qual seu formulário se baseia. Por exemplo, você pode querer implementar um formulário para reagendar uma reunião, e seu formulário é baseado em um formulário existente para agendar reuniões. Se a cadeia de caracteres da classe de mensagem do formulário de agendamento da reunião for "IPM. Reunião ", sua cadeia de caracteres de classe de mensagem pode ser" IPM. Meeting. Reschedule ".
    
- Se o formulário não for baseado em qualquer formulário existente, a cadeia de caracteres de classe da mensagem ainda deverá começar com a "IPM". ou "IPC". prefixo, dependendo se o formulário deve ser recebido por uma pessoa ou por outro aplicativo. "IPM". designa uma mensagem interpessoal que geralmente acaba na caixa de entrada de um usuário e "IPC". designa uma mensagem de comunicação entre processos que normalmente não é entregue à caixa de entrada de um usuário.
    
- Se a sua classe de mensagens pretende ser legível, a cadeia de caracteres da classe da mensagem deve começar com "IPM". Uma classe de mensagem geralmente é considerada legível se usa qualquer propriedade que contenha dados de texto sem formatação, HTML ou Rich Text Format (RTF). Se o formulário usar a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), deve-se quase certamente usar uma "IPM." Cadeia de caracteres de classe de mensagem. Por exemplo, se você estiver implementando um formulário para ordens de compra e sua organização exigir que as ordens de compra sejam aprovadas por um gerente, sua cadeia de caracteres de classe de mensagem poderá ser "IPM. Purchase_Order ". Os formulários projetados para uso com pastas públicas ou aplicativos de pasta pública são normalmente considerados como interpessoais, pois eles são lidos por pessoas, mesmo que eles não sejam realmente endereçados ao endereço de email de qualquer pessoa. O prefixo típico para classes de mensagem de pasta pública é "IPM. Post ". 
    
- Se a sua classe de mensagens pretende ser recebida por outro aplicativo, e não por uma pessoa, a cadeia de caracteres da classe da mensagem deve começar com "IPC". Por exemplo, se você estiver implementando um formulário que permite às pessoas se inscrever automaticamente nas listas de endereçamento, sua cadeia de caracteres de classe de mensagem pode ser "IPC. Inscrever ".
    
- Sua cadeia de caracteres de classe de mensagem nunca deve terminar com um ponto.
    
A cadeia de caracteres de classe da mensagem deve ser colocada na seção **[Description]** do arquivo de configuração de **** formulário, na entrada MessageClass, semelhante à seguinte: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Após escolher uma cadeia de caracteres de classe de mensagem apropriada, você deve gerar um identificador de classe para ela. Os identificadores de classe podem ser gerados com o comando **Create GUID** incluído no Visual Studio. O identificador de classe deve ser colocado na entrada **CLSID** do arquivo de configuração de formulário, juntamente com a entrada MessageClass, similar à seguinte: **** 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
O identificador de classe quase certamente será diferente, naturalmente. Para obter mais informações, consulte [criar um arquivo de configuração de formulário](creating-a-form-configuration-file.md).
  
Quando o formulário é instalado no computador de um usuário, seu processo de instalação — seja um programa de instalação ou outra coisa — deve fazer uma entrada de registro na seção **\* HKEY_CLASSES_ROOT\CLSID* do registro para o identificador de classe. Essa entrada deve ser definida como a cadeia de caracteres da classe de mensagem. Por exemplo, crie uma entrada de registro semelhante à seguinte para o exemplo de identificador de classe acima: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obter mais informações, consulte [instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Confira também



[Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

