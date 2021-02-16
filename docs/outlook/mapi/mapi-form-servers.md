---
title: Servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 855292b8-028e-4c1e-87ed-3f20b9ba584a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3c95f6a1d4d50dd6552c6e786d17c40da14f3f3c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419104"
---
# <a name="mapi-form-servers"></a>Servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Da perspectiva do usuário, um formulário geralmente é uma folha de propriedades para uma mensagem ou um formulário de entrada de dados que permite aos usuários inserir informações estruturadas. No entanto, pode ser qualquer interface do usuário associada a uma classe de mensagem. Do ponto de vista de um programador, um formulário consiste em:
  
- Um tipo de mensagem MAPI com sua própria classe de mensagem e identificador OLE.
    
- O arquivo executável que implementa o servidor de formulário.
    
- Uma coleção de propriedades MAPI — personalizadas ou de outra forma — que o servidor de formulário usa. Alguns ou todos eles podem estar disponíveis para clientes de mensagens para uso.
    
- O arquivo de configuração que descreve o formulário e é usado pelo gerenciador de formulário.
    
Como os formulários são [objetos IMessage,](imessageimapiprop.md) eles exibem propriedades e comportamento consistentes com objetos de mensagem MAPI. No entanto, como os formulários podem ter propriedades personalizadas, controles e uma renderização de exibição específica do aplicativo, as interfaces MAPI que os formulários usam são genéricas o suficiente para permitir qualquer tipo de interface necessária. A definição real de um formulário é armazenada em uma biblioteca de formulário, o que é discutido posteriormente nesta seção. 
  
> [!NOTE]
> Mais precisamente, todas as mensagens são instâncias de formulários MAPI. No entanto, geralmente é mais fácil pensar em formulários personalizados como casos especiais de mensagens, já que formulários para composição e leitura de mensagens de email típicas são os formulários mais usados. O fato de que todas as mensagens são apenas formulários fornece aos formulários personalizados o mesmo status de qualquer outra mensagem no sistema MAPI. 
  
Cada formulário tem um conjunto de propriedades, algumas das quais são visíveis na interface do usuário do formulário. Normalmente, as propriedades são corresponder aos campos na interface do usuário do formulário. Por exemplo, um formulário de pedido de compra pode ter os campos Item, Descrição, Preço, Imposto e Subtotal. Esses campos são simplesmente renderizações visuais de propriedades de formulário com os mesmos nomes. Os clientes garantem quais propriedades são suportadas por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcFormPropSet,](imapiforminfo-calcformpropset.md) que é implementado pelo gerenciador de formulário MAPI. 
  
Assim como as mensagens básicas, os formulários MAPI podem conter todas as propriedades de mensagem padrão, como o remetente, o destinatário pretendido e quando a mensagem foi enviada. Os formulários também podem conter qualquer número de propriedades personalizadas específicas do formulário. Por exemplo, um formulário "Relatório de Bugs" pode conter propriedades personalizadas para Tipo de Bug, Severidade de Bug e Versão do Produto.
  
Para criar um formulário, você deve implementar um servidor de formulário. O servidor de formulário é o arquivo executável carregado quando um cliente de mensagens precisa exibir uma mensagem que é do tipo suportado pelo servidor de formulário. O servidor de formulário, por sua vez, cria objetos de formulário conforme necessário para exibir mensagens específicas e manipular interações do usuário com essas mensagens.
  
Cada servidor de formulário tem um arquivo de configuração associado a ele. Esse arquivo contém informações que descrevem o servidor de formulário para o benefício do gerenciador de formulário. O gerenciador de formulário usa essas informações ao instalar o servidor de formulário em uma biblioteca de formulário.
  
Para obter detalhes sobre como criar as partes de um formulário, consulte [Developing MAPI Form Servers](developing-mapi-form-servers.md).
  
Os servidores de formulário aderem ao Com (Component Object Model). Os servidores de formulário são executados como executáveis autônomos, não como servidores in-proc. Para obter mais informações, consulte a seção COM e ActiveX Object Services no SDK do Windows.
  
Um identificador de classe exclusivo (CLSID) identifica cada servidor de formulário. Sempre há um mapeamento um para um entre um identificador de classe e sua classe de mensagem. Isso não significa, no entanto, que um servidor de formulário só pode trabalhar com mensagens de uma classe de mensagem. Se nenhum servidor de formulário estiver disponível para fazer o serviço de uma mensagem de uma classe específica, o gerenciador de formulário que está sendo usado deve tentar encontrar um servidor de formulário para uma classe de mensagem mais alto na hierarquia de classe de mensagens; o gerenciador de formulário padrão fornecido com o SDK do Windows faz isso. Esse servidor de formulário provavelmente poderá renderizar apenas um subconjunto das propriedades da mensagem (aquelas com suporte da superclasse), mas será melhor do que nada. O que acontece quando nenhum servidor de formulário correspondente é encontrado é um detalhe de implementação específico do gerenciador de formulário que está sendo usado; o gerenciador de formulário padrão não abre mensagens quando isso acontece.
  
Para obter mais informações, consulte [CLASSES de mensagens MAPI.](mapi-message-classes.md)
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

