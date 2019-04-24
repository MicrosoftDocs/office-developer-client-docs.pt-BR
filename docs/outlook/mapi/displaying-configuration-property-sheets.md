---
title: Exibir a configuração das folhas de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a796f458e9d30206dc4c6feb37cbdb1e6b6a704b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316398"
---
# <a name="displaying-configuration-property-sheets"></a>Exibir a configuração das folhas de propriedades

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de transporte usam o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para implementar as folhas de propriedades de configuração. Ao chamar **DoConfigPropSheet**, o provedor de transporte passa em um ponteiro para uma matriz de propriedades junto com informações sobre como exibi-las. Em seguida, o MAPI apresenta as propriedades para o usuário por meio de uma caixa de diálogo padrão. É altamente recomendável que você use este mecanismo de folha de propriedades ao implementar seu provedor de transporte devido aos benefícios para o usuário de uma interface consistente.
  
## <a name="transport-providers"></a>Provedores de transporte

Os provedores de transporte podem usar a função [BuildDisplayTable](builddisplaytable.md) para simplificar a construção de uma tabela de exibição para uso com o **DoConfigPropSheet**. Os provedores de transporte também podem usar a API da folha de propriedades diretamente. Para armazenar as alterações nas propriedades, os provedores de transporte podem usar a função [CreateIProp](createiprop.md) . Isso simplifica a manipulação de cancelamentos pelo usuário enquanto o usuário modifica os valores armazenados nas propriedades. Se necessário, um provedor de transporte também pode fornecer uma caixa de diálogo de assistente para simplificar tarefas de configuração para o usuário. 
  

