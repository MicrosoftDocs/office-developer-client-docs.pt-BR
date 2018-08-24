---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584335"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera a posição da linha de tabela atual do cursor, com base em um valor fracionário.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parâmetros

 _lpulRow_
  
> [out] Ponteiro para o número da linha atual. O número da linha é baseado em zero; a primeira linha da tabela é zero. 
    
 _lpulNumerator_
  
> [out] Ponteiro para o numerador da fração identifica a posição da tabela.
    
 _lpulDenominator_
  
> [out] Ponteiro para o denominador da fração identifica a posição da tabela. O parâmetro _lpulDenominator_ não pode ser zero. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O método retornados valores válidos em _lpulRow_, _lpulNumerator_e _lpulDenominator_.
    
## <a name="remarks"></a>Comentários

O método **IMAPITable::QueryPosition** determina a posição da linha atual e retorna o número de linha atual e um valor fracionário indicando sua posição relativa ao final da tabela. MAPI define a linha atual como a próxima linha a ser lido. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Não é necessário retornar o número exato de linhas na tabela para o parâmetro _lpulDenominator_ ; pode ser uma aproximação. 
  
Se você não puder determinar a linha atual, retorne um valor 0xFFFFFFFF em _lpulRow_.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **QueryPosition** para posicionar uma caixa de rolagem em uma barra de rolagem. Por exemplo, em uma tabela que contém a 100 linhas, se **QueryPosition** retorna um valor de 75 no parâmetro _lpulNumerator_ , 100 no parâmetro _lpulDenominator_ e 75 no parâmetro _lpulRow_ , você pode posicionar a caixa de rolagem 3/4 de a maneira como entre a barra de rolagem. 
  
Não confie no valor do _lpulDenominator_ sendo o número de linhas da tabela. **QueryPosition** sempre não pode identificar a linha exata que o cursor é posicionado sobre. 
  
Uma chamada para **QueryPosition** pode envolver grandes quantidades de memória, especialmente para tabelas categorizadas grandes. Se o parâmetro _lpulRow_ é definido como 0xFFFFFFFF, muita memória era necessária para **QueryPosition** determinar a linha atual. Chame o método [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) para posicionar a tabela na linha identificadas pelos parâmetros _lpulNumerator_ e _lpulDenominator_ . No entanto, não sempre espera **SeekRowApprox** para estabelecer a mesma linha **que QueryPosition** teria se memória não tivesse sido um fator como a posição atual. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

