---
title: Escolhendo uma classe de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428050"
---
# <a name="choosing-a-message-class"></a>Escolhendo uma classe de mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conforme descrito em Classes de [Mensagens MAPI,](mapi-message-classes.md)as classes de mensagens são importantes para estabelecer a relação entre os tipos de mensagens personalizadas e, por extensão, entre os próprios servidores de formulário. Felizmente, escolher uma cadeia de caracteres de classe de mensagem é bastante simples. A cadeia de caracteres de classe de mensagem de uma classe de mensagem é uma cadeia de caracteres arbitrária, mas deve usar as seguintes convenções:
  
- A cadeia de caracteres deve atender a todas as convenções descritas na documentação para a **propriedade PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). Importante, a cadeia de caracteres deve ser composta inteiramente de caracteres ANSI e ter menos de 256 caracteres.
    
- Se o servidor de formulário é derivado de um servidor de formulário existente ou é uma extensão de um servidor de formulário existente, sua cadeia de caracteres de classe de mensagem deve ser formada adicionando um ponto e outra palavra à cadeia de caracteres de classe de mensagem do servidor de formulário no que seu formulário se baseia. Por exemplo, talvez você queira implementar um formulário para reagendar uma reunião, e seu formulário se baseia em um formulário existente para agendar reuniões. Se a cadeia de caracteres de classe de mensagem do formulário de agendamento de reunião for "IPM. Reunião", sua cadeia de caracteres de classe de mensagem pode ser "IPM. Meeting.Reschedule".
    
- Se o formulário não for baseado em nenhum formulário existente, sua cadeia de caracteres de classe de mensagem ainda deverá começar com "IPM". ou "IPC". prefixo, dependendo se o formulário deve ser recebido por uma pessoa ou por outro aplicativo. "IPM". designa uma mensagem interpersonal que geralmente termina na Caixa de Entrada de um usuário e "IPC". designa uma mensagem de comunicação entre processos que normalmente não é entregue à Caixa de Entrada de um usuário.
    
- Se a classe de mensagem tiver o objetivo de ser acessível para humanos, a cadeia de caracteres da classe de mensagem deverá começar com "IPM". Uma classe de mensagem geralmente é considerada legível por humanos se ela usar qualquer propriedade que contenha dados de texto sem formatação, HTML ou RTF (Rich Text Format). Se seu formulário usa a **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), ele certamente deve usar um "IPM". cadeia de caracteres de classe de mensagem. Por exemplo, se você estiver implementando um formulário para pedidos de compra e sua organização exigir que os pedidos de compra sejam aprovados por um gerente, sua cadeia de caracteres de classe de mensagem pode ser "IPM. Purchase_Order". Formulários projetados para uso com pastas públicas ou aplicativos de pasta pública são geralmente considerados interpersonalos porque são lidos por pessoas, mesmo que não sejam endereçados a endereços de email de qualquer pessoa. O prefixo típico para classes de mensagem de pasta pública é "IPM. Post". 
    
- Se a classe de mensagem deve ser recebida por outro aplicativo em vez de uma pessoa, a cadeia de caracteres da classe de mensagem deve começar com "IPC". Por exemplo, se você estiver implementando um formulário que permita que as pessoas assinem automaticamente listas de mensagens, sua cadeia de caracteres de classe de mensagem pode ser "IPC. Subscribe".
    
- Sua cadeia de caracteres de classe de mensagem nunca deve terminar com um ponto.
    
A cadeia de caracteres de classe de mensagem deve ser colocada na seção **[Descrição]** do arquivo de configuração do formulário, na entrada **MessageClass,** semelhante ao seguinte: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Depois de escolher uma cadeia de caracteres de classe de mensagem apropriada, você deve gerar um identificador de classe para ela. Os identificadores de classe podem ser gerados com **o comando** Criar GUID incluído no Visual Studio. O identificador de classe deve ser colocado na entrada **CLSID** do arquivo de configuração do formulário, juntamente com a entrada **MessageClass,** semelhante ao seguinte: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Seu identificador de classe certamente será diferente, é claro. Para obter mais informações, consulte [Criando um arquivo de configuração de formulário.](creating-a-form-configuration-file.md)
  
Quando o formulário é *instalado \** no computador de um usuário, o processo de instalação — seja um programa de instalação ou outra coisa — deve fazer uma entrada do Registro na seção *HKEY_CLASSES_ROOT\CLSIDdo Registro para o identificador de classe. Essa entrada deve ser definida como a cadeia de caracteres de classe de mensagem. Por exemplo, você criaria uma entrada do Registro semelhante à seguinte para o identificador de classe de exemplo acima: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obter mais informações, [consulte Instalando um formulário em uma biblioteca.](installing-a-form-into-a-library.md)
  
## <a name="see-also"></a>Confira também



[Desenvolvendo servidores de formulário MAPI](developing-mapi-form-servers.md)

