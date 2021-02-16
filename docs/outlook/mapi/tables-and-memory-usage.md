---
title: Tabelas e o uso da memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436857"
---
# <a name="tables-and-memory-usage"></a>Tabelas e o uso da memória

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um problema importante conectado à recuperação de dados de uma tabela é o uso da memória. A falta de memória disponível pode causar falha em [IMAPITable::QueryRows](imapitable-queryrows.md) e [HrQueryAllRows,](hrqueryallrows.md) retornando menos do que o número desejado de linhas. Decidir qual método ou função usar para recuperar dados de tabela depende se a tabela deve caber na memória e, se não puder, se a falha for aceitável. 
  
Como nem sempre é fácil determinar a quantidade de dados que caberá na memória de uma só vez, o MAPI fornece algumas diretrizes básicas para que um provedor de serviços ou aplicativo cliente siga. Lembre-se de que sempre há exceções, com base na implementação de tabela específica e em como os dados subjacentes são armazenados.
  
As diretrizes a seguir podem ser usadas para avaliar o uso da memória da tabela:
  
- Clientes que podem tolerar o uso ocasional de memória do conjunto de trabalho no intervalo de megabyte e podem supor que não terão problemas ao ler uma tabela inteira na memória. 
    
- As restrições afetam o uso de memória de uma tabela. Uma tabela gravemente restrita com um grande número de linhas, como uma tabela de conteúdo, pode ser esperada para caber na memória enquanto uma tabela grande irrestrita normalmente não pode. 
    
- Várias das tabelas pertencentes a MAPI, como status, perfil, serviço de mensagens, provedor e tabelas de armazenamento de mensagens, geralmente caberão na memória. Geralmente, são tabelas pequenas. No entanto, há exceções. Por exemplo, um provedor de perfil baseado em servidor pode gerar uma tabela de perfil maior que não será capaz de caber.
    
Para recuperar todas as linhas de uma tabela que caberá na memória sem problemas, chame [HrQueryAllRows](hrqueryallrows.md), definindo o número máximo de linhas como zero.
  
Para recuperar todas as linhas de uma tabela que pode ou não caber na memória, gerando um erro, chame **HrQueryAllRows** especificando um número máximo de linhas. O número máximo de linhas deve ser definido como um número maior do que o número mínimo de linhas necessárias. Se um cliente tiver que acessar pelo menos 50 linhas de uma tabela de 300 linhas, o número máximo de linhas deverá ser definido como pelo menos 51. 
  
Para recuperar todas as linhas de uma tabela que não deve caber na memória, chame [IMAPITable::QueryRows](imapitable-queryrows.md) em um loop com uma contagem de linhas relativamente pequena, como ilustra o exemplo de código a seguir: 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

Quando esse loop for concluído e todas as linhas da tabela foram processadas e  _cRows_ for zero, a posição do cursor normalmente estará na parte inferior da tabela. 
  
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

