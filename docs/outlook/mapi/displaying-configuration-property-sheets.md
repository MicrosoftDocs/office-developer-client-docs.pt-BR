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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421309"
---
# <a name="displaying-configuration-property-sheets"></a>Exibir a configuração das folhas de propriedades

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de transporte usam [o método IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para implementar folhas de propriedades de configuração. Ao chamar **DoConfigPropSheet**, o provedor de transporte passa um ponteiro para uma matriz de propriedades juntamente com informações sobre como exibi-las. MAPI, em seguida, apresenta as propriedades ao usuário por meio de uma caixa de diálogo padrão. É fortemente incentivado a usar esse mecanismo de folha de propriedades ao implementar seu provedor de transporte devido ao benefício para o usuário de uma interface consistente.
  
## <a name="transport-providers"></a>Provedores de transporte

Os provedores de transporte podem usar a [função BuildDisplayTable](builddisplaytable.md) para simplificar a construção de uma tabela de exibição para uso com **DoConfigPropSheet**. Os provedores de transporte também podem usar a API da folha de propriedades diretamente. Para fazer alterações de buffer nas propriedades, os provedores de transporte podem usar [a função CreateIProp.](createiprop.md) Isso simplifica o tratamento de cancelamentos pelo usuário enquanto o usuário modifica os valores armazenados nas propriedades. Se necessário, um provedor de transporte também pode fornecer uma caixa de diálogo do assistente para simplificar as tarefas de configuração para o usuário. 
  

