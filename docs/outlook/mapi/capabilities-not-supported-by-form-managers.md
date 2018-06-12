---
title: Recursos não suportados pelos gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 86c91353b620482ca0862aa998aae1b3329cfc94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766240"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Recursos não suportados pelos gerentes de formulário

  
  
**Aplica-se a**: Outlook 
  
Os seguintes recursos não são suportados pelo gerente de formulário padrão por motivos de desempenho, mas podem ser suportados pelos gerentes de formulário personalizado.
  
- Uma hierarquia que permite que os formulários a serem agrupadas ou categorizados em toda uma biblioteca de formulários. Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.
    
- Controle de acesso para categorias de formulários, correspondente às classes de mensagem ou superclasse.
    
- Suporte para várias versões de idioma do mesmo formulário em uma biblioteca de formulário simples.
    
Esses são os problemas de implementação. Não há nada para impedir que um gerente de formulário personalizado com a implementação desses recursos.
  
A arquitetura de formulário MAPI não oferece suporte a vários gerentes de formulário executando simultaneamente. Embora MAPI ofereça suporte a vários provedores de armazenamento de mensagem simultâneas, provedores de transporte e provedores de catálogo de endereços, somente um Gerenciador de formulário simples é suportado.
  
Porque o Gerenciador de apenas um formulário pode estar em execução ao mesmo tempo, se você implementar um gerente de formulário personalizado, você terá a reimplementação qualquer funcionalidade do Gerenciador de formulário padrão que você precisa. Porque seu gerente de formulário personalizado inteiramente substituirá o Gerenciador de formulário padrão, os recursos do Gerenciador de formulário padrão só estará disponíveis a menos que eles são duplicados em seu gerente de formulário personalizado.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

