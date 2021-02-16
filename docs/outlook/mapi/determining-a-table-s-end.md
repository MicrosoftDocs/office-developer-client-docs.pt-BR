---
title: Determinando o final de uma tabela
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
# <a name="determining-a-tables-end"></a>Determinando o final de uma tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Um erro comum é presumir que o final da tabela foi atingido quando: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o final do loop determinado pela contagem de linhas retornada por [IMAPITable::GetRowCount](imapitable-getrowcount.md). A contagem **retornada por GetRowCount** nem sempre representa o número exato de linhas na tabela; é uma contagem aproximada. 
    
- **QueryRows** foi chamado com um número fixo de linhas e menos linhas são retornadas. It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve. 
    
> [!IMPORTANT]
> A única vez que um chamador pode assumir que o cursor está posicionado no final da tabela para uma contagem de linhas positiva ou no início da tabela para uma contagem de linhas negativas é quando o valor S_OK e zero linhas são retornadas. O valor MAPI_E_NOT_FOUND é retornado. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

