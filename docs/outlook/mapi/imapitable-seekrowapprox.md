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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412146"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Move o cursor para uma posição fracionada aproximada na tabela. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parâmetros

 _ulNumerator_
  
> [in] Ponteiro para o numerador da fração que representa a posição da tabela. Se o  _parâmetro ulNumerator_ for zero, o cursor será posicionado no início da tabela, independentemente do valor do denominador. Se  _ulNumerator for_ igual ao  _parâmetro ulDenominator,_ o cursor será posicionado após a última linha da tabela. 
    
 _ulDenominator_
  
> [in] Ponteiro para o denominador da fração que representa a posição da tabela. O  _parâmetro ulDenominator_ não pode ser zero. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de busca foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede o início da operação de busca de linha. A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.
    
## <a name="remarks"></a>Comentários

A posição do cursor em uma tabela após uma chamada para o método **IMAPITable::SeekRowApprox** é heuristicamente a fração e pode não ser exata. Por exemplo, certos provedores podem implementar uma tabela sobre uma árvore binária, tratando o ponto de metade da tabela como parte superior da árvore por motivos de desempenho. Se a árvore não estiver equilibrada, o ponto de metade usado pode não estar exatamente no meio da tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SeekRowApprox para** fornecer os dados para uma implementação de barra de rolagem. Por exemplo, se o usuário posicionar a caixa de rolagem 2/3 abaixo da barra de rolagem, você poderá modelar essa ação chamando **SeekRowApprox** e passando um valor fracionado equivalente usando  _ulNumerator_ e  _ulDenominator_. A **pesquisa SeekRowApprox** é sempre absoluta desde o início da tabela. Para mover para o final da tabela, os valores em  _ulNumerator_ e  _ulDenominator_ devem ser os mesmos. 
  
Use qualquer esquema de números apropriado. Ou seja, para procurar uma posição no meio da tabela, você pode especificar 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)

