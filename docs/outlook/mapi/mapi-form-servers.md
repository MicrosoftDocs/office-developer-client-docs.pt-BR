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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351482"
---
# <a name="mapi-form-servers"></a>Servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Da perspectiva do usuário, um formulário é geralmente uma folha de propriedades para uma mensagem ou um formulário de entrada de dados que permite que os usuários insiram informações estruturadas. No enTanto, pode ser qualquer interface do usuário associada a uma classe de mensagem. Do ponto de vista de um programador, um formulário consiste em:
  
- Um tipo de mensagem MAPI com sua própria classe de mensagem e identificador OLE.
    
- O arquivo executável que implementa o servidor de formulário.
    
- Uma coleção de propriedades MAPI, personalizada ou não, que o servidor de formulário usa. Alguns ou todos eles podem estar disponíveis para os clientes de mensagens para uso.
    
- O arquivo de configuração que descreve o formulário e é usado pelo Gerenciador de formulários.
    
Como os formulários são objetos [IMessage](imessageimapiprop.md) , eles exibem as propriedades e o comportamento que são consistentes com os objetos de mensagem MAPI. No enTanto, como os formulários podem ter propriedades personalizadas, controles e uma renderização de exibição específica do aplicativo, as interfaces MAPI que os formulários usam são genéricas o suficiente para permitir qualquer tipo de interface necessário. A definição real de um formulário é armazenada em uma biblioteca de formulários, que é abordada posteriormente nesta seção. 
  
> [!NOTE]
> Mais precisamente, todas as mensagens são instâncias de formulários MAPI. No enTanto, geralmente é mais fácil pensar em formulários personalizados como casos especiais de mensagens, já que os formulários para compor e ler mensagens de email típicas são os formulários mais comumente usados. O fato de que todas as mensagens são, na verdade, apenas os formulários personalizados dão o mesmo status de qualquer outra mensagem no sistema MAPI. 
  
Todo formulário tem um conjunto de propriedades, alguns dos quais estão visíveis na interface do usuário do formulário. Normalmente, as propriedades são correspondidas aos campos na interface do usuário do formulário. Por exemplo, um formulário de ordem de compra pode ter os campos item, descrição, Price, Tax e subTotal. Esses campos são apenas processamentos visuais de propriedades de formulário de mesmo nome. Os clientes determinam quais propriedades são suportadas por uma determinada classe de mensagens por meio do método [IMAPIFormInfo:: CalcFormPropSet](imapiforminfo-calcformpropset.md) , que é implementado pelo Gerenciador de formulários MAPI. 
  
Como as mensagens básicas, os formulários MAPI podem conter todas as propriedades de mensagem padrão, como o remetente, o destinatário desejado e quando a mensagem foi enviada. Formulários também podem conter qualquer número de propriedades personalizadas que são específicas para o formulário. Por exemplo, um formulário "relatório de erros" pode conter Propriedades personalizadas para tipo de bug, severidade de bug e versão do produto.
  
Para criar um formulário, você deve implementar um servidor de formulários. O servidor de formulário é o arquivo executável que é carregado quando um cliente de mensagens precisa exibir uma mensagem que é o tipo suportado pelo servidor de formulários. O servidor de formulário, por sua vez, cria objetos de formulário, conforme necessário, para exibir mensagens específicas e lidar com as interações do usuário com essas mensagens.
  
Todos os servidores de formulário têm um arquivo de configuração associado a ele. Este arquivo contém informações que descrevem o servidor de formulário para obter o benefício do Gerenciador de formulários. O gerente de formulários usa essas informações ao instalar o servidor de formulário em uma biblioteca de formulários.
  
Para obter detalhes sobre como criar as partes de um formulário, consulte [developING MAPI Form Servers](developing-mapi-form-servers.md).
  
Os servidores de formulário aderem ao modelo de objeto de componente (COM). Os servidores de formulário são executados como executáveis autônomos, não como servidores em processamento. Para obter mais informações, consulte a seção serviços de objeto COM e ActiveX no SDK do Windows.
  
Um identificador de classe exclusivo (CLSID) identifica cada servidor de formulário. Sempre há um mapeamento de um-para-um entre um identificador de classe e sua classe de mensagem. No entanto, isso não significa que um servidor de formulário só possa funcionar com mensagens de uma classe de mensagem. Se nenhum servidor de formulário estiver disponível para atender a uma mensagem de uma determinada classe, o Gerenciador de formulários que está sendo usado deve tentar localizar um servidor de formulário para uma classe de mensagem superior na hierarquia de classe de mensagem; o Gerenciador de formulários padrão fornecido com o Windows SDK faz isso. Esse servidor de formulário provavelmente será capaz de renderizar apenas um subconjunto das propriedades da mensagem (os que têm suporte na superclasse), mas será melhor do que Nothing. O que acontece quando nenhum servidor de formulário correspondente é encontrado em todos é um detalhe de implementação específico para o Gerenciador de formulários que está sendo usado; o Gerenciador de formulários padrão não abrirá mensagens quando isso acontecer.
  
Para obter mais informações, consulte [MAPI Message classes](mapi-message-classes.md).
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

