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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415660"
---
# <a name="imapitablequeryposition"></a>IMAPITable::QueryPosition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera a posição atual da linha da tabela do cursor, com base em um valor fracionado.
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a>Parâmetros

 _lpulRow_
  
> [out] Ponteiro para o número da linha atual. O número da linha é baseado em zero; a primeira linha na tabela é zero. 
    
 _lpulNumerator_
  
> [out] Ponteiro para o numerador para a fração que identifica a posição da tabela.
    
 _lpulDenominator_
  
> [out] Ponteiro para o denominador da fração que identifica a posição da tabela. O  _parâmetro lpulDenominator_ não pode ser zero. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O método retornou valores válidos  _em lpulRow_,  _lpulNumerator_ e  _lpulDenominator_.
    
## <a name="remarks"></a>Comentários

O **método IMAPITable::QueryPosition** determina a posição da linha atual e retorna o número da linha atual e um valor fracionado indicando sua posição relativa ao final da tabela. MAPI define a linha atual como a próxima linha a ser lida. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não é necessário retornar o número exato de linhas na tabela para o parâmetro  _lpulDenominator;_ pode ser uma aproximação. 
  
Se você não puder determinar a linha atual, retorne um valor de 0xFFFFFFFF em  _lpulRow_.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode usar **QueryPosition para** posicionar uma caixa de rolagem em uma barra de rolagem. Por exemplo, em uma tabela contendo 100 linhas, se **QueryPosition** retornar um valor de 75 no parâmetro  _lpulNumerator,_ 100 no parâmetro  _lpulDenominator_ e 75 no parâmetro  _lpulRow,_ você poderá posicionar a caixa de rolagem 3/4 do caminho pela barra de rolagem. 
  
Não confie no valor em  _lpulDenominator_ sendo o número de linhas na tabela. **QueryPosition** nem sempre pode identificar a linha exata na qual o cursor está posicionado. 
  
Uma chamada para **QueryPosition pode** envolver grandes quantidades de memória, especialmente para tabelas categorizadas grandes. Se o  _parâmetro lpulRow_ estiver definido como 0xFFFFFFFF, muita memória foi necessária para **que QueryPosition** determine a linha atual. Chame o método [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) para posicionar a tabela na linha identificada pelos parâmetros _lpulNumerator_ e _lpulDenominator._ No entanto, nem sempre espere **que SeekRowApprox** estabeleça como a posição atual a mesma **linha que QueryPosition** teria se a memória não tivesse sido um fator. 
  
## <a name="see-also"></a>Confira também



[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

