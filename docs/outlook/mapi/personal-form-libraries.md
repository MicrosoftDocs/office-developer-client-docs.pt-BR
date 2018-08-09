---
title: Bibliotecas de formulários pessoais
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768212"
---
# <a name="personal-form-libraries"></a>Bibliotecas de formulários pessoais

  
  
**Aplica-se a**: Outlook 
  
Como seu nome sugere, bibliotecas de formulários particulares contêm formulários de interesse para um usuário específico. Biblioteca de formulários particular do usuário é a biblioteca de formulários associada ao repositório de mensagem padrão identificado no perfil do usuário; cada perfil instalado em uma estação de trabalho pode usar um repositório separado padrão e, portanto, uma biblioteca de formulários particulares separado. Uma biblioteca de formulários particulares pode conter cópias das formas que também estão contidas em outras bibliotecas de formulários, além de outras formas.
  
Uma biblioteca de formulários particular é implementada na tabela de conteúdo associados da pasta raiz no armazenamento de mensagens do usuário padrão — se que reside em um servidor ou localmente na estação de trabalho do usuário é irrelevante. Se o armazenamento de mensagens padrão do usuário é armazenado na estação de trabalho do usuário, bibliotecas de formulários particulares oferecem desempenho aprimorado, permitindo que aplicativos acessem os formulários localmente, em vez de pela rede. Ele também disponibiliza formulários para usuários trabalhando offline, que podem ocorrer quando os usuários desejam assumir suas formas com eles em computadores portáteis e são sem acesso a uma rede.
  
As propriedades e implementação subjacente de entradas de biblioteca de formulários particulares incluem uma propriedade de "Contêiner ID" que identifica um contêiner de mestre que a entrada de local deve ser sincronizada com. Isso pode ser o identificador de uma pasta arbitrária que contém formulários. Isso é útil se você estiver usando um gerente de formulário personalizado que ofereça suporte a algum tipo de biblioteca de formulários de toda a organização; o gerente do formulário seria cuidam da sincronização de formulários armazenados na biblioteca de formulários particulares e a biblioteca de formulários de toda a organização. Isso provavelmente ocorrerá quando o Gerenciador de formulário foi carregado, mas pode acontecer teoricamente a qualquer momento.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

