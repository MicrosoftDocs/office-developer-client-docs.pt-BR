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
ms.openlocfilehash: 0b73e246ad5e396ef67e89bff5f1e04a47f6ebcb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569922"
---
# <a name="mapi-form-servers"></a>Servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Da perspectiva do usuário, o formulário é geralmente uma folha de propriedades para uma mensagem ou um formulário de entrada de dados que permite que os usuários insiram as informações estruturadas. No entanto, pode ser qualquer interface do usuário que está associado uma classe de mensagem. Do ponto de vista do programador, um formulário consiste em:
  
- Um tipo de mensagem MAPI com seu próprio classe da mensagem e o identificador OLE.
    
- O arquivo executável que implementa o servidor do formulário.
    
- Uma coleção de propriedades MAPI — personalizados ou caso contrário — que usa o servidor de formulário. Alguns ou todos esses podem estar disponíveis para clientes de mensagens para uso.
    
- O arquivo de configuração que descreve o formulário e é usado pelo Gerenciador do formulário.
    
Como os formulários são objetos [IMessage](imessageimapiprop.md) , eles exibem propriedades e o comportamento é consistente com objetos de mensagem MAPI. No entanto, como formulários podem ter uma renderização de exibição que é específico do aplicativo, controles e propriedades personalizadas, as interfaces MAPI que o uso de formulários estão genéricas para permitir que qualquer tipo de interface que é necessária. A definição real de um formulário é armazenada em uma biblioteca de formulários, que é abordada posteriormente nesta seção. 
  
> [!NOTE]
> Mais precisamente, todas as mensagens são instâncias de formulários MAPI. No entanto, é geralmente mais fácil pensar formulários personalizados como casos especiais de mensagens, desde formulários para redigir e leitura de mensagens de email típica é mais comumente usadas formulários. O mesmo status de qualquer outra mensagem de formulários do fato de que todas as mensagens são realmente apenas oferece de formulários personalizados no sistema de MAPI. 
  
Cada formulário tem um conjunto de propriedades, algumas das quais estão visíveis na interface do usuário do formulário. Geralmente, as propriedades são comparadas aos campos na interface de usuário do formulário. Por exemplo, um formulário de pedido de compra pode ter os campos do Item, descrição, preço, imposto e Subtotal. Esses campos são simplesmente visuais renderizações de propriedades de formulário, os mesmos nomes. Clientes averiguar quais propriedades são suportadas por uma classe de mensagem específica por meio do método [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md) , que é implementado pelo gerente de formulário de MAPI. 
  
Como mensagens básicas, formulários MAPI podem conter todas as propriedades de mensagem padrão como remetente, destinatário, e quando a mensagem foi enviada. Formulários também podem conter qualquer número de propriedades personalizadas que são específicas para o formulário. Por exemplo um formulário de "Relatório de Bug" pode conter propriedades personalizadas para o tipo de Bug, gravidade do Bug e versão do produto.
  
Para criar um formulário, você deve implementar um servidor de formulário. O servidor de formulário é o arquivo executável que é carregado quando um cliente de mensagens precisa para exibir uma mensagem que é o tipo suportado pelo servidor de formulário. Por sua vez, o servidor de formulário cria objetos de formulário conforme o necessário para exibir mensagens específicas e manipular interações do usuário com essas mensagens.
  
Cada servidor do formulário tem um arquivo de configuração associado a ela. Esse arquivo contém informações que descrevem o servidor de formulário em benefício o gerente do formulário. O Gerenciador de formulário usa essas informações ao instalar o servidor de formulário em uma biblioteca de formulários.
  
Para obter detalhes sobre como criar as partes de um formulário, consulte [Desenvolvimento de servidores de formulário de MAPI](developing-mapi-form-servers.md).
  
Servidores de formulário aderem para o modelo COM (Component Object). Servidores de formulário são executados como executáveis autônomo, e não como servidores na proc. Para obter mais informações, consulte a seção de serviços de objetos ActiveX e COM no SDK do Windows.
  
Um identificador exclusivo de classe (CLSID) identifica a cada servidor do formulário. Sempre existe um mapeamento individual entre um identificador de classe e sua classe de mensagem. Isso significa, no entanto, se um servidor de formulário só pode trabalhar com mensagens da classe de uma mensagem. Se nenhum servidor do formulário está disponível para uma mensagem de uma determinada classe de serviço, o gerente de formulário que está sendo usado deverá tentar localizar um servidor de formulário para uma classe de mensagem acima na hierarquia de classe da mensagem; o Gerenciador de formulário padrão fornecido com o SDK do Windows faz isso. Desses servidores de formulário provavelmente será capaz de renderizar apenas um subconjunto das propriedades da mensagem (aqueles suportados pelo superclasse), mas ele será melhor do que nada. O que acontece quando nenhum servidor de formulário correspondente for encontrado em todos os é um detalhe da implementação específico para o gerente do formulário que está sendo usado; o Gerenciador de formulário padrão não abrem mensagens quando isso acontece.
  
Para obter mais informações, consulte [Classes de mensagem MAPI](mapi-message-classes.md).
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

