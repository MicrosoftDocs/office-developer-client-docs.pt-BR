---
title: Tabelas e uso de memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770587"
---
# <a name="tables-and-memory-usage"></a>Tabelas e uso de memória

**Aplica-se a**: Outlook 
  
Uma questão importante conectada com a recuperação de dados de uma tabela é o uso de memória. Falta de memória disponível pode causar [IMAPITable:: QueryRows](imapitable-queryrows.md) e [HrQueryAllRows](hrqueryallrows.md) falha, retornando menor do que o número de linhas desejado. Decidir qual método ou a função a ser usada para recuperar dados da tabela depende se a tabela pode ser esperada para ajustá-la na memória e se for possível, se a falha é aceitável. 
  
Porque nem sempre é fácil determinar a quantidade de dados que se ajustarão à memória ao mesmo tempo, MAPI fornece algumas diretrizes básicas para um aplicativo cliente ou o provedor de serviço a seguir. Lembre-se de que sempre há exceções, com base em como os dados subjacentes são armazenados e a implementação de determinada tabela.
  
As diretrizes a seguir podem ser usadas para avaliar o uso de memória da tabela:
  
- Os clientes que podem tolerar ocasionais uso de memória de conjunto de trabalho no intervalo megabyte e podem assumir que eles têm problemas de leitura de uma tabela inteira na memória. 
    
- Restrições tem um efeito sobre o uso de uma tabela de memória. Para ajustá-la na memória enquanto uma tabela grande unrestricted geralmente não pode, espera-se uma tabela está seriamente restrita com um amplo número de linhas, como uma tabela de conteúdo. 
    
- Várias tabelas do pertencentes a MAPI, como status, perfil, o serviço de mensagem, provedor e tabelas de repositório de mensagens, geralmente couberem na memória. Estas são as tabelas geralmente é pequenas. No entanto, há exceções. Por exemplo, um provedor de perfil baseado em servidor pode gerar uma tabela maior de perfil que não será possível para ajustá-la.
    
Para recuperar todas as linhas de uma tabela que se ajustarão à memória sem problemas, chame [HrQueryAllRows](hrqueryallrows.md), definindo o número máximo de linhas a zero.
  
Para recuperar todas as linhas de uma tabela que pode ou não pode cabem na memória, gerar um erro, chame **HrQueryAllRows** especificando um número máximo de linhas. O número máximo de linhas deve ser definido para um número maior que o número mínimo de linhas que são necessários. Se um cliente deve acessar pelo menos 50 linhas de uma tabela de 300 linha, o número máximo de linhas deve ser definido como 51 pelo menos. 
  
Para recuperar todas as linhas de uma tabela que não é esperada para ajustá-la na memória, chame [IMAPITable:: QueryRows](imapitable-queryrows.md) em um loop com uma contagem de linha relativamente pequeno, como mostra o exemplo de código a seguir: 
  
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

Quando este loop for concluído e todas as linhas na tabela foram processadas e _pássaros_ é zero, geralmente será a posição do cursor na parte inferior da tabela. 
  
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

