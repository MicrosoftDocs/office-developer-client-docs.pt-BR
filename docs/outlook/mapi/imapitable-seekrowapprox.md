---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328837"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Move o cursor para uma posição fracionária aproximada na tabela. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parâmetros

 _ulNumerator_
  
> no Ponteiro para o numerador da fração que representa a posição da tabela. Se o parâmetro _ulNumerator_ for zero, o cursor será posicionado no início da tabela, independente do valor do denominador. Se _ulNumerator_ for igual ao parâmetro _ulDenominator_ , o cursor será posicionado após a última linha da tabela. 
    
 _ulDenominator_
  
> no Ponteiro para o denominador da fração que representa a posição da tabela. O parâmetro _ulDenominator_ não pode ser zero. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de busca foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento, o que impede a inicialização da operação de busca da linha. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

A posição do cursor em uma tabela após uma chamada para o método imApitable **:: SeekRowApprox** é a fração heurística e pode não ser exata. Por exemplo, determinados provedores podem implementar uma tabela na parte superior de uma árvore binária, tratando o ponto intermediário da tabela como a parte superior da árvore por motivos de desempenho. Se a árvore não for balanceada, o ponto intermediário usado poderá não ser exatamente no meio da tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SeekRowApprox** para fornecer os dados de uma implementação de barra de rolagem. Por exemplo, se o usuário posicionar a caixa de rolagem 2/3 para baixo na barra de rolagem, você poderá modelar essa ação chamando **SeekRowApprox** e passando um valor fracionário equivalente usando o _UlNumerator_ e o _ulDenominator_. A pesquisa do **SeekRowApprox** sempre é absoluta do início da tabela. Para mover para o final da tabela, os valores em _ulNumerator_ e _ulDenominator_ devem ser os mesmos. 
  
Use qualquer esquema de números apropriado. Ou seja, para buscar uma posição na metade da tabela, você pode especificar 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)

