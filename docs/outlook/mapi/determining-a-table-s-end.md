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
ms.openlocfilehash: 7cbf11f16948d582ba36a0b4d20411549b723b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766402"
---
# <a name="determining-a-tables-end"></a>Determinar o fim de uma tabela

  
  
**Aplica-se a**: Outlook 
  
 Um erro comum é pressupõem que o fim da tabela foi alcançado quando: 
  
- [IMAPITable:: QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o fim do loop determinado pela contagem de linhas retornada pela [IMAPITable::GetRowCount](imapitable-getrowcount.md). A contagem de **GetRowCount** retorna nem sempre representam o número exato de linhas da tabela. é uma contagem aproximada. 
    
- **QueryRows** tenha sido chamado com um número fixo de linhas e menos linhas são retornadas. É não até **QueryRows** retorna uma linha definidas com uma contagem de linhas igual a zero não existem mais linhas para recuperar. 
    
> [!IMPORTANT]
> A única vez que um chamador pode assumir que o cursor é posicionado no final da tabela para uma contagem de linha positivo ou no início da tabela para uma contagem de linha negativo é quando o valor S_OK e zero linhas são retornadas. O valor E_NOT_FOUND nunca será retornado. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

