---
title: Obter e definir várias propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 150f2a55bff4188c1f692de8276ed869bcf66c3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766658"
---
# <a name="getting-and-setting-multiple-properties"></a>Obter e definir várias propriedades

**Aplica-se a**: Outlook 
  
Obtendo e definindo propriedades quantos possíveis com o menor número de chamadas, remotas atividade é curtailed e a sobrecarga envolvida com cada propriedade é reduzida. Embora os provedores de serviços tentarem coletar propriedades antes de fazer uma chamada de procedimento remoto para recuperação ou modificação, você pode otimizar desse esforço solicitando-se começar com várias propriedades.
  
Por exemplo, se você trabalha com listas de roteamento que descrevem os destinatários futuros com propriedades nomeadas que pertencem aos conjuntos de propriedade específica, processe todos os destinatários com duas chamadas. Use uma chamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar os identificadores para todas as propriedades do destinatário e a outra chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos os valores. A alternativa, fazendo uma chamada para **GetIDsFromNames** seguido por uma chamada para **GetProps** para cada destinatário, é muito menos eficiente. 
  

