---
title: Recursos incompatíveis com gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a84c0a93f80080b71f6049e73f0a0094c38c28ef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566870"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Recursos incompatíveis com gerentes de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os seguintes recursos não são suportados pelo gerente de formulário padrão por motivos de desempenho, mas podem ser suportados pelos gerentes de formulário personalizado.
  
- Uma hierarquia que permite que os formulários a serem agrupadas ou categorizados em toda uma biblioteca de formulários. Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.
    
- Controle de acesso para categorias de formulários, correspondente às classes de mensagem ou superclasse.
    
- Suporte para várias versões de idioma do mesmo formulário em uma biblioteca de formulário simples.
    
Esses são os problemas de implementação. Não há nada para impedir que um gerente de formulário personalizado com a implementação desses recursos.
  
A arquitetura de formulário MAPI não oferece suporte a vários gerentes de formulário executando simultaneamente. Embora MAPI ofereça suporte a vários provedores de armazenamento de mensagem simultâneas, provedores de transporte e provedores de catálogo de endereços, somente um Gerenciador de formulário simples é suportado.
  
Porque o Gerenciador de apenas um formulário pode estar em execução ao mesmo tempo, se você implementar um gerente de formulário personalizado, você terá a reimplementação qualquer funcionalidade do Gerenciador de formulário padrão que você precisa. Porque seu gerente de formulário personalizado inteiramente substituirá o Gerenciador de formulário padrão, os recursos do Gerenciador de formulário padrão só estará disponíveis a menos que eles são duplicados em seu gerente de formulário personalizado.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

