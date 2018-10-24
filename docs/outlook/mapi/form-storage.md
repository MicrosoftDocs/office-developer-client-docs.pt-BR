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
ms.openlocfilehash: c98427ab326ada0b717282dc4077d526780aa45c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568158"
---
# <a name="form-storage"></a>Armazenamento de formulários

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Embora não seja necessário saber todos os detalhes de como os formulários são fisicamente armazenados, é útil compreender alguns dos principais conceitos. Portanto, antes de descrever os três tipos de bibliotecas de formulários compatíveis com o Gerenciador de formulário padrão, este tópico oferece uma visão geral de como os formulários são armazenados.
  
Definições de formulário podem ser armazenadas fisicamente dentro de pastas em um ou mais repositórios de mensagem MAPI. Cada pasta MAPI pode ser considerada como tendo duas áreas para armazenar os objetos de mensagem: o parte padrão e a parte associada. O parte padrão da pasta inclui as mensagens e pastas que os usuários manipular.
  
A parte associada inclui objetos de mensagem oculta que estão associados à pasta, inclusive as definições do formulário, modos de exibição, modelos de regras, modelos de resposta e assim por diante. Nesta parte alternativa é chamada de tabela de conteúdo associados a pasta e o conjunto de mensagens na tabela de conteúdo associado é conhecido como as informações associadas a pasta. As mensagens ocultas são uma parte integrante da pasta e são copiadas juntamente com o conteúdo da pasta padrão quando a pasta é copiada. Embora fisicamente armazenados como mensagens, informações na tabela de conteúdo associado de uma pasta se comporta como propriedades vez like mensagens visíveis. Qualquer objeto folder que ofereça suporte a uma tabela de conteúdo associado é capaz de armazenar formulários personalizados. O método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pode retornar o conteúdo padrão ou o conteúdo associado da pasta, dependendo do valor do parâmetro de _ulflags_ do método. 
  
Uma biblioteca de formulários consiste em definições do formulário armazenadas na tabela de conteúdo associado de uma pasta. A definição do formulário inclui as propriedades do formulário, as ações que o formulário oferece suporte e até mesmo o formulário server arquivo executável, que é armazenado como um ou mais anexos da mensagem.
  
Além disso, os formulários podem ser armazenados em qualquer arquivo ou local que suporta o Gerenciador de formulário que está sendo usado. O Gerenciador de formulário padrão armazena os servidores de formulário em pastas de MAPI, mas um gerente de formulário personalizado poderia implementar seu próprio armazenamento para servidores de formulário.
  
Um formulário pode ter várias interfaces de usuário que são vinculados a classe da mensagem. Por exemplo, um formulário pode ter interfaces de usuário separadas de redação e leitura. A cuida de formulário de chamar a interface de usuário apropriados para solicitações de usuário diferente, dependendo de qual dos verbos do formulário está sendo chamada. Por exemplo, se o servidor do formulário tiver redigir separado e leitura de interfaces de usuário, a interface do usuário de redação pode ser aberta automaticamente quando o usuário cria uma nova mensagem da classe de mensagem do formulário e a interface do usuário de leitura pode ser aberta automaticamente quando o usuário abre uma mensagem existente da classe de mensagem do formulário.
  
A maioria das informações armazenadas dentro de uma definição de formulário está disponível, chamando o método [IMAPIFormInfo::IMAPIProp](imapiforminfoimapiprop.md) em um objeto **IMAPIFormInfo** . A interface **IMAPIFormInfo** simplifica o acesso às informações de formulário chamando-se todos os métodos necessários para recuperar as informações de mensagem e pasta MAPI. Um objeto **IMAPIFormInfo** pode ser obtido chamando o método [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) . 
  
Os três tipos de bibliotecas de formulários são descritos nos tópicos [Local bibliotecas de formulários](local-form-libraries.md), [Bibliotecas de formulários de pasta](folder-form-libraries.md) e [Bibliotecas de formulários particulares](personal-form-libraries.md).
  
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)

