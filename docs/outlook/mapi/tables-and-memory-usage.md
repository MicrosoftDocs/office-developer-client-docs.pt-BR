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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320402"
---
# <a name="tables-and-memory-usage"></a>Tabelas e o uso da memória

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um problema importante conectado à recuperação de dados de uma tabela é o uso de memória. A falta de memória disponível pode causar imApitable [:: QueryRows](imapitable-queryrows.md) e [HrQueryAllRows](hrqueryallrows.md) falhar, retornando menos do que o número desejado de linhas. Decidir qual método ou função usar para recuperar os dados da tabela dependerá se a tabela pode ser adequada para caber na memória e, se não puder, se a falha for aceitável. 
  
Como nem sempre é fácil determinar a quantidade de dados que se ajustarão na memória de uma só vez, o MAPI fornecerá algumas diretrizes básicas para um aplicativo cliente ou provedor de serviços a seguir. Lembre-se de que há sempre exceções, com base na implementação específica da tabela e como os dados subjacentes são armazenados.
  
As diretrizes a seguir podem ser usadas para avaliar o uso da memória da tabela:
  
- Os clientes que podem tolerar o uso de memória de conjunto de trabalho ocasional no intervalo de megabytes e podem supor que não terão problemas para ler uma tabela inteira na memória. 
    
- As restrições afetam o uso da memória de uma tabela. Uma tabela rigorosamente restrita com um grande número de linhas, como uma tabela de conteúdo, pode ser esperado para caber na memória, enquanto uma tabela grande irrestrita não é possível. 
    
- Várias das tabelas pertencentes a MAPI, como o status, o perfil, o serviço de mensagens, o provedor e as tabelas de repositório de mensagens, normalmente se encaixarão na memória. Geralmente são tabelas pequenas. No enTanto, há exceções. Por exemplo, um provedor de perfil baseado em servidor pode gerar uma tabela de perfil maior que não poderá se ajustar.
    
Para recuperar todas as linhas de uma tabela que se ajustam à memória sem problemas, chame [HrQueryAllRows](hrqueryallrows.md), definindo o número máximo de linhas como zero.
  
Para recuperar todas as linhas de uma tabela que podem ou não se ajustar à memória, gerando um erro, chame **HrQueryAllRows** especificando um número máximo de linhas. O número máximo de linhas deve ser definido como um número maior que o número mínimo de linhas necessárias. Se um cliente precisar acessar pelo menos 50 linhas de uma tabela de linha 300, o número máximo de linhas deverá ser definido como pelo menos 51. 
  
Para recuperar todas as linhas de uma tabela que não seja adequada para a memória, chame imApitable [:: QueryRows](imapitable-queryrows.md) em um loop com uma contagem de linha relativamente pequena, pois o exemplo de código a seguir ilustra: 
  
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

Quando esse loop é concluído e todas as linhas da tabela foram processadas e as _galinha_ são zero, a posição do cursor normalmente estará na parte inferior da tabela. 
  
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

