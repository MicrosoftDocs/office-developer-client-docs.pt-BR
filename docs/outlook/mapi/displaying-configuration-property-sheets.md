---
title: Exibindo as folhas de propriedades de configuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588353"
---
# <a name="displaying-configuration-property-sheets"></a>Exibindo as folhas de propriedades de configuração

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de transporte usam o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para implementar folhas de propriedades de configuração. Ao chamar **DoConfigPropSheet**, o provedor de transporte passa em um ponteiro para uma matriz de propriedades, juntamente com informações sobre como exibi-los. MAPI apresenta as propriedades para o usuário por meio de uma caixa de diálogo padrão. Você é altamente encorajado usar esse mecanismo de folha de propriedade ao implementar o seu provedor de transporte devido a vantagem para o usuário de uma interface consistente.
  
## <a name="transport-providers"></a>Provedores de transporte

Provedores de transporte podem usar a função [BuildDisplayTable](builddisplaytable.md) para simplificar a construção de uma tabela de exibição para uso com **DoConfigPropSheet**. Provedores de transporte também podem usar a API de folha de propriedade diretamente. As alterações nas propriedades de buffer, provedores de transporte pode usar a função [CreateIProp](createiprop.md) . Isso simplifica a manipulação de cancelamentos pelo usuário enquanto o usuário modifica os valores armazenados nas propriedades. Se necessário, um provedor de transporte também pode fornecer uma caixa de diálogo Assistente caixa para simplificar as tarefas de configuração para o usuário. 
  

