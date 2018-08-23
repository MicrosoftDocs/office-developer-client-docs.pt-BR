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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572080"
---
# <a name="imapitableseekrowapprox"></a>IMAPITable::SeekRowApprox

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Move o cursor para uma posição fracional aproximada na tabela. 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a>Parâmetros

 _ulNumerator_
  
> [in] Ponteiro para o numerador da fração que representa a posição da tabela. Se o parâmetro _ulNumerator_ for zero, o cursor é posicionado no início da tabela independente do valor do denominador. Se não for igual ao parâmetro _ulDenominator_ _ulNumerator_ , o cursor é posicionado após a última linha da tabela. 
    
 _ulDenominator_
  
> [in] Ponteiro para o denominador da fração que representa a posição da tabela. O parâmetro _ulDenominator_ não pode ser zero. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de busca foi bem-sucedida.
    
MAPI_E_BUSY 
  
> Outra operação está em andamento que impede que a linha que buscam início da operação. Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.
    
## <a name="remarks"></a>Comentários

A posição do cursor em uma tabela depois de uma chamada para o método **IMAPITable:: SeekRowApprox** heuristicamente é a fração e pode não ser exata. Por exemplo, certos provedores podem implementar uma tabela na parte superior de uma árvore binária, tratando ponto intermediário da tabela como parte superior da árvore por motivos de desempenho. Se a árvore não é balanceada, em seguida, o ponto intermediário usado pode não ser exatamente na metade a tabela. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SeekRowApprox** para fornecer os dados para uma implementação da barra de rolagem. Por exemplo, se o usuário posiciona o 2/3 de caixa de rolagem para baixo da barra de rolagem, você pode modelar essa ação chamando **SeekRowApprox** e passando um valor fracionário equivalente usando _ulNumerator_ e _ulDenominator_. A pesquisa **SeekRowApprox** é sempre absoluta desde o início da tabela. Para mover para o final da tabela, os valores em _ulNumerator_ e _ulDenominator_ devem ser o mesmo. 
  
Use o esquema de qualquer número é apropriado. Ou seja, para buscar para uma posição na metade a tabela, você pode especificar 1/2, 10/20 ou 50/100. 
  
## <a name="see-also"></a>Confira também



[IMAPITable : IUnknown](imapitableiunknown.md)

