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
  
Os seguintes recursos não são suportados pelo gerenciador de formulário padrão por motivos de desempenho, mas podem ser suportados por gerentes de formulário personalizados.
  
- Uma hierarquia que permite que formulários sejam agrupados ou categorizados em uma biblioteca de formulários. Uma biblioteca de formulários é um banco de dados de arquivos simples de formulários.
    
- Controle de acesso para categorias de formulários, correspondente a classes de mensagens ou superclasses.
    
- Suporte para várias versões de idioma do mesmo formulário em uma única biblioteca de formulário.
    
Esses são os problemas de implementação. Não há nada para impedir que um gerenciador de formulário personalizado implemente esses recursos.
  
A arquitetura de formulário MAPI não dá suporte a vários gerentes de formulário sendo executados simultaneamente. Embora o MAPI seja compatível com vários provedores simultâneos de armazenamento de mensagens, provedores de transporte e de agendas de endereços, apenas um único gerenciador de formulário é suportado.
  
Because only one form manager may be running at once, if you implement a custom form manager you will have to re-implement any functionality from the default form manager that you need. Como o gerenciador de formulário personalizado substituirá totalmente o gerenciador de formulário padrão, os recursos do gerenciador de formulário padrão estarão indisponíveis, a menos que sejam duplicados no gerenciador de formulário personalizado.
  
## <a name="see-also"></a>Confira também



[Formulários MAPI](mapi-forms.md)

