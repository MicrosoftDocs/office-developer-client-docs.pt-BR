---
title: Recursos não suportados por gerentes de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b51e9e03-a333-4fdc-b6fe-87bd4e947b9f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e31eacaae54968fbdbd9fe0345130a8d09c3509f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419377"
---
# <a name="capabilities-not-supported-by-form-managers"></a>Recursos não suportados por gerentes de formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os recursos a seguir não são suportados pelo Gerenciador de formulários padrão por motivos de desempenho, mas podem ser suportados por gerentes de formulários personalizados.
  
- Uma hierarquia que permite que os formulários sejam agrupados ou categorizados em uma biblioteca de formulários. Uma biblioteca de formulários é um banco de dados de arquivo simples de formulários.
    
- Controle de acesso para categorias de formulários, correspondentes a classes de mensagens ou superclasses.
    
- Suporte para versões de vários idiomas do mesmo formulário em uma única biblioteca de formulários.
    
Estes são problemas de implementação. Não há nada para impedir que um gerente de formulário personalizado implemente esses recursos.
  
A arquitetura de formulário MAPI não dá suporte a vários gerentes de formulários executados simultaneamente. Embora o MAPI dê suporte a vários provedores de repositório de mensagens simultâneos, provedores de transporte e provedores de catálogo de endereços, só há suporte para um único Gerenciador de formulários.
  
Como apenas um gerente de formulário pode ser executado ao mesmo tempo, se você implementar um gerente de formulário personalizado, será necessário reimplementar qualquer funcionalidade do Gerenciador de formulários padrão que você precisa. Como o gerente de formulário personalizado substituirá totalmente o Gerenciador de formulários padrão, os recursos do Gerenciador de formulários padrão não estarão disponíveis, a menos que sejam duplicados no seu gerente de formulário personalizado.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

