---
title: Obter e configurar várias propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299374"
---
# <a name="getting-and-setting-multiple-properties"></a>Obter e configurar várias propriedades

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ao obter e definir o máximo de propriedades possível com o menor número de chamadas, a atividade remota é curtailed e a sobrecarga envolvida com cada propriedade é reduzida. Embora os provedores de serviços tentem coletar as propriedades antes de fazer uma chamada de procedimento remoto para recuperação ou modificação, você pode otimizar esse esforço solicitando várias propriedades para começar.
  
Por exemplo, se você trabalhar com listas de roteamento que descrevem destinatários futuros com propriedades nomeadas pertencentes a determinados conjuntos de propriedades, processe todos os destinatários com duas chamadas. Use uma chamada para [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar os identificadores de todas as propriedades de destinatário e a outra chamada para [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar todos os valores. A alternativa, fazendo uma chamada para **GetIDsFromNames** seguida de uma chamada para **** GetProps para cada destinatário, é muito menos eficiente. 
  

