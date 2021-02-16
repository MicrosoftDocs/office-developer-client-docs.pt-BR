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
  
Embora não seja necessário saber todos os detalhes de como os formulários são fisicamente armazenados, é útil entender alguns dos principais conceitos. Portanto, antes de descrever os três tipos de bibliotecas de formulários com suporte do gerenciador de formulários padrão, este tópico fornece uma visão geral de como os formulários são armazenados.
  
As definições de formulário podem ser armazenadas fisicamente em pastas em um ou mais armazenamentos de mensagens MAPI. Cada pasta MAPI pode ser pensada como tendo duas áreas para armazenar objetos de mensagem: a parte padrão e a parte associada. A parte padrão da pasta inclui as mensagens e pastas que os usuários manipulam.
  
A parte associada inclui objetos de mensagem ocultos que estão associados à pasta, incluindo definições de formulário, exibições, modelos de regra, modelos de resposta e assim por diante. Essa parte alternativa é chamada de tabela de conteúdo associada à pasta, e o conjunto de mensagens na tabela de conteúdo associada é conhecido como as informações associadas à pasta. As mensagens ocultas são uma parte integral da pasta e são copiadas junto com o conteúdo padrão da pasta quando a pasta é copiada. Embora seja fisicamente armazenada como mensagens, as informações na tabela de conteúdo associada de uma pasta se comportam mais como propriedades do que como mensagens que podem ser visualizadas. Qualquer objeto de pasta que suporte uma tabela de conteúdo associada é capaz de armazenar formulários personalizados. O [método IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pode retornar o conteúdo padrão ou o conteúdo associado da pasta, dependendo do valor do parâmetro  _lags_ do método. 
  
Uma biblioteca de formulário consiste em definições de formulário armazenadas na tabela de conteúdo associada de uma pasta. A definição de formulário inclui as propriedades do formulário, as ações aceitas pelo formulário e até mesmo o arquivo executável do servidor de formulário, que é armazenado como um ou mais anexos de mensagem.
  
Além disso, os formulários podem ser armazenados em qualquer arquivo ou local ao suporte do gerenciador de formulários que está sendo usado. O gerenciador de formulário padrão armazena servidores de formulário em pastas MAPI, mas um gerenciador de formulário personalizado pode implementar seu próprio armazenamento para servidores de formulário.
  
Um formulário pode ter várias interfaces de usuário que estão vinculadas à sua classe de mensagem. Por exemplo, um formulário pode ter interfaces de usuário de Redação e Leitura separadas. O formulário se ocupa de invocar a interface de usuário adequada para diferentes solicitações de usuário, dependendo de quais verbos do formulário estão sendo chamados. For example, if your form server has separate composing and reading user interfaces, the Compose user interface can be opened automatically when the user creates a new message of the form's message class and the Read user interface can be opened automatically when the user opens an existing message of the form's message class.
  
A maioria das informações armazenadas em uma definição de formulário está disponível invocando o método [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) em um objeto **IMAPIFormInfo.** A interface **IMAPIFormInfo** simplifica o acesso às informações do formulário chamando todos os métodos de mensagem e pasta MAPI necessários para recuperar as informações. Um **objeto IMAPIFormInfo** pode ser obtido chamando o método [IMAPIFormContainer::ResolveMessageClass.](imapiformcontainer-resolvemessageclass.md) 
  
The three types of form libraries are described in the topics [Local Form Libraries](local-form-libraries.md), [Folder Form Libraries](folder-form-libraries.md) and [Personal Form Libraries](personal-form-libraries.md).
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

