---
title: Determinando o fim de uma tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420084"
---
# <a name="determining-a-tables-end"></a>Determinando o fim de uma tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Um erro comum é supor que o final da tabela tenha sido alcançado quando: 
  
- [IMAPITable:: QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o final do loop determinado pela contagem de linhas retornado por [IMAPITable:: GetRowCount](imapitable-getrowcount.md). A contagem que **** o GetRowCount retorna nem sempre representa o número exato de linhas na tabela; é uma contagem aproximada. 
    
- **QueryRows** foi chamado com um número fixo de linhas e menos linhas são retornadas. Não é até que **QueryRows** retorna um conjunto de linhas com uma contagem de linha igual a zero que não há mais linhas a serem recuperadas. 
    
> [!IMPORTANT]
> O único momento em que um chamador pode supor que o cursor está posicionado no final da tabela para uma contagem de linha positiva ou no início da tabela para uma contagem de linhas negativas é quando o valor S_OK e as linhas zero são retornados. O valor MAPI_E_NOT_FOUND nunca é retornado. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

