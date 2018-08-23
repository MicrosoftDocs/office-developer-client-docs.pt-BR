---
title: Determinar o fim de uma tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f9979baf144b6106adcec416ee04439404e05d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576341"
---
# <a name="determining-a-tables-end"></a>Determinar o fim de uma tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Um erro comum é pressupõem que o fim da tabela foi alcançado quando: 
  
- [IMAPITable:: QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o fim do loop determinado pela contagem de linhas retornada pela [IMAPITable::GetRowCount](imapitable-getrowcount.md). A contagem de **GetRowCount** retorna nem sempre representam o número exato de linhas da tabela. é uma contagem aproximada. 
    
- **QueryRows** tenha sido chamado com um número fixo de linhas e menos linhas são retornadas. É não até **QueryRows** retorna uma linha definidas com uma contagem de linhas igual a zero não existem mais linhas para recuperar. 
    
> [!IMPORTANT]
> A única vez que um chamador pode assumir que o cursor é posicionado no final da tabela para uma contagem de linha positivo ou no início da tabela para uma contagem de linha negativo é quando o valor S_OK e zero linhas são retornadas. O valor E_NOT_FOUND nunca será retornado. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

