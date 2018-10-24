---
title: Escolher uma classe de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c3b486838c6ce2d7fc38d950a4de6f4589767073
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574234"
---
# <a name="choosing-a-message-class"></a>Escolher uma classe de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conforme descrito nas [Classes de mensagem MAPI](mapi-message-classes.md), classes de mensagens são importantes para estabelecer a relação entre os tipos de mensagens personalizadas e, por extensão, entre os próprios servidores do formulário. Felizmente, escolher uma cadeia de caracteres de classe de mensagem é razoavelmente simple. A cadeia de caracteres de classe de mensagem de uma classe de mensagem é uma cadeia de caracteres arbitrária, mas ela deve usar as convenções a seguir:
  
- A cadeia de caracteres deve satisfazer a todas as convenções descritas na documentação da propriedade **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)). É importante, a cadeia de caracteres deve ser composto inteiramente de caracteres ANSI e ter menos de 256 caracteres.
    
- Se seu servidor de formulário é derivado de um servidor existente do formulário ou é uma extensão de um servidor de formulário existente, sua cadeia de caracteres de classe de mensagem deve ser formada por meio da adição de um período e outra palavra para a cadeia de caracteres de classe de mensagem do servidor do formulário que seu formulário se baseia em. Por exemplo, talvez você queira implementar um formulário para reagendar uma reunião e seu formulário se baseia em um formulário existente para programar reuniões. Se a reunião agendamento de cadeia de caracteres de classe de mensagem do formulário for "IPM. Reunião", sua cadeia de caracteres de classe de mensagem poderia ser"IPM. Meeting.Reschedule".
    
- Se o formulário não é baseado em qualquer formulário existente, sua cadeia de caracteres de classe de mensagem ainda deve começar com um do "formulário IPM." ou "CPI." prefixo, dependendo se o formulário é destinado a ser recebido por uma pessoa ou por outro aplicativo. "IPM." designa uma mensagem interpessoais que geralmente termina na caixa de entrada do usuário e "CPI." designa uma mensagem de comunicação entre processos que normalmente não é entregue à caixa de entrada do usuário.
    
- Se sua classe de mensagem destina-se para ser legíveis, a cadeia de caracteres de classe de mensagem deve começar com "IPM." Uma classe de mensagem geralmente é considerada legíveis se ele usa todas as propriedades que contêm texto sem formatação, HTML, ou dados de formato Rich Text (RTF). Se o formulário usar a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), ele deve usar certamente "IPM." cadeia de caracteres de classe de mensagem. Por exemplo, se você estiver implementando um formulário para ordens de compra e sua organização requer que as ordens de compra sejam aprovados por um gerente, sua cadeia de caracteres de classe de mensagem poderia ser "IPM. Purchase_Order". Formulários que são projetados para usam com pastas públicas ou aplicativos de pasta pública normalmente são considerados como estando interpessoais porque eles são lidos por pessoas, mesmo que não são abordadas realmente para o endereço de email de qualquer pessoa. O prefixo típico para classes de mensagens de pasta pública é "IPM. POST". 
    
- Se sua classe de mensagem se destina a ser recebido por outro aplicativo, em vez de por uma pessoa, a cadeia de caracteres de classe de mensagem deve começar com "CPI." Por exemplo, se você estiver implementando um formulário que permite que as pessoas automaticamente se inscrever para listas de endereçamento, sua cadeia de caracteres de classe de mensagem poderia ser "CPI. Inscrever-se".
    
- Sua cadeia de caracteres de classe de mensagem nunca deve terminar com um ponto.
    
A cadeia de caracteres de classe de mensagem deve ser colocada na seção **[descrição]** do arquivo de configuração de formulário, na entrada **MessageClass** , semelhante ao seguinte: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Depois que você escolheu uma cadeia de caracteres de classe de mensagem apropriada, você deve gerar um identificador de classe para ele. Identificadores de classe podem ser gerados com o comando **Criar GUID** que está incluído no Visual Studio. O identificador de classe deve ser colocado na entrada do **CLSID** do arquivo de configuração de formulário, juntamente com a **MessageClass** entrada, semelhante ao seguinte: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
O identificador de classe certamente será diferente, é claro. Para obter mais informações, consulte [Criando um arquivo de configuração do formulário](creating-a-form-configuration-file.md).
  
Quando o formulário está instalado no computador do usuário, o processo de instalação — se ela é um programa de instalação ou outra coisa — deve realizar uma entrada de registro no **HKEY_CLASSES_ROOT\CLSID\* * seção do registro para o identificador de classe. Essa entrada deve ser definida como a cadeia de caracteres de classe de mensagem. Por exemplo, você deve criar uma entrada de registro semelhante ao seguinte para o identificador de classe do exemplo acima: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Para obter mais informações, consulte [Instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de servidores de formulário MAPI](developing-mapi-form-servers.md)

