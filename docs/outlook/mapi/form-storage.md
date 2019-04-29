---
title: Armazenamento de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ddf9158-3c10-408a-aeaf-5a382c4339e7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 793a34b093ba69f73be7e186bec0a769584bbac4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414890"
---
# <a name="form-storage"></a>Armazenamento de formulários

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora não seja necessário conhecer todos os detalhes de como os formulários são armazenados fisicamente, é útil entender alguns dos principais conceitos. Portanto, antes de descrever os três tipos de bibliotecas de formulários compatíveis com o Gerenciador de formulários padrão, este tópico fornece uma visão geral de como os formulários são armazenados.
  
As definições de formulário podem ser armazenadas fisicamente em pastas em um ou mais repositórios de mensagens MAPI. Todas as pastas MAPI podem ser consideradas como tendo duas áreas para o armazenamento de objetos de mensagem: a parte padrão e a parte associada. A parte padrão da pasta inclui as mensagens e pastas que os usuários manipulam.
  
A parte associada inclui objetos de mensagem ocultos associados à pasta, incluindo definições de formulário, modos de exibição, modelos de regra, modelos de resposta e assim por diante. Essa parte alternativa é denominada tabela de conteúdo associado à pasta e o conjunto de mensagens na tabela de conteúdo associado é conhecido como as informações associadas à pasta. As mensagens ocultas são uma parte integral da pasta e são copiadas junto com o conteúdo da pasta padrão quando a pasta é copiada. Embora sejam armazenadas fisicamente como mensagens, as informações na tabela de conteúdo associado de uma pasta se comparecem com propriedades semelhantes às de mensagens visíveis. Qualquer objeto Folder que dê suporte a uma tabela de conteúdo associado é capaz de armazenar formulários personalizados. O método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable pode retornar o conteúdo padrão ou o conteúdo associado da pasta, dependendo do valor do parâmetro _parâmetroulflags_ do método. 
  
Uma biblioteca de formulários consiste em definições de formulário armazenadas na tabela de conteúdo associada de uma pasta. A definição de formulário inclui as propriedades do formulário, as ações que o formulário suporta e até mesmo o arquivo executável do servidor de formulário, que é armazenado como um ou mais anexos de mensagem.
  
Além disso, os formulários podem ser armazenados em qualquer arquivo ou local ao qual o gerente de formulário esteja sendo usado ofereça suporte. O Gerenciador de formulários padrão armazena servidores de formulário em pastas MAPI, mas um gerente de formulário personalizado pode implementar seu próprio armazenamento para servidores de formulário.
  
Um formulário pode ter várias interfaces de usuário vinculadas à sua classe de mensagem. Por exemplo, um formulário pode ter interfaces de usuário de redação e leitura separadas. O formulário cuida da invocação da interface do usuário adequada para diferentes solicitações de usuário, dependendo de qual dos verbos do formulário está sendo chamado. Por exemplo, se o seu servidor de formulário tiver uma composição separada e a leitura de interfaces de usuário, a interface de usuário de redação poderá ser aberta automaticamente quando o usuário criar uma nova mensagem da classe de mensagem do formulário e a interface do usuário de leitura puder ser aberta automaticamente quando o o usuário abre uma mensagem existente da classe de mensagem do formulário.
  
A maioria das informações armazenadas em uma definição de formulário está disponível invocando o método [IMAPIFormInfo:: IMAPIProp](imapiforminfoimapiprop.md) em um objeto **IMAPIFormInfo** . A interface **IMAPIFormInfo** simplifica o acesso a informações de formulário chamando todos os métodos de mensagens e pastas MAPI necessários para recuperar as informações. Um objeto **IMAPIFormInfo** pode ser obtido chamando o método [IMAPIFormContainer:: ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Os três tipos de bibliotecas de formulários são descritos nas [bibliotecas de formulários locais](local-form-libraries.md)de tópicos, [bibliotecas de formulários de pastas](folder-form-libraries.md) e bibliotecas de [formulários pessoais](personal-form-libraries.md).
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

