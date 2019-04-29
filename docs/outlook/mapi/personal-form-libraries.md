---
title: Bibliotecas de formulários pessoais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420406"
---
# <a name="personal-form-libraries"></a>Bibliotecas de formulários pessoais

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como o nome sugere, as bibliotecas de formulários pessoais contêm formas de interesse para um usuário específico. A biblioteca de formulários pessoais de um usuário é a biblioteca de formulários associada ao repositório de mensagens padrão identificado no perfil do usuário; cada perfil instalado em uma estação de trabalho pode usar um repositório padrão separado e, portanto, uma biblioteca de formulários particulares separada. Uma biblioteca de formulários pessoais pode conter cópias de formulários que também estão contidas em outras bibliotecas de formulários, além de outros formulários.
  
Uma biblioteca de formulários pessoais é implementada na tabela de conteúdo associado da pasta raiz no repositório de mensagens padrão de um usuário, independentemente de ele residir em um servidor ou localmente na estação de trabalho do usuário. Se o repositório de mensagens padrão do usuário estiver armazenado na estação de trabalho do usuário, as bibliotecas de formulários pessoais oferecem um desempenho aprimorado, permitindo que os aplicativos acessem os formulários localmente, em vez de através da rede. Ele também disponibiliza os formulários aos usuários que trabalham offline, o que pode ocorrer quando os usuários desejam usar seus formulários em computadores portáteis e estão sem acesso a uma rede.
  
As propriedades e a implementação subjacente das entradas da biblioteca de formulários pessoais incluem uma propriedade "ID do contêiner" que identifica um contêiner mestre com o qual a entrada local deve ser sincronizada. Pode ser o identificador de uma pasta arbitrária que contém formulários. Isso é útil se você estiver usando um Gerenciador de formulários personalizado que oferece suporte a algum tipo de biblioteca de formulários em toda a organização; o gerente de formulários cuidaria da sincronização dos formulários armazenados na biblioteca de formulários pessoais e da biblioteca de formulários em toda a organização. Isso provavelmente aconteceria quando o Gerenciador de formulários foi carregado, mas pode, teoricamente, acontecer a qualquer momento.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

