---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407498"
---
# <a name="itnefextractprops"></a>ITnef::ExtractProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Extrai as propriedades de um encapsulamento TNEF. 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como as propriedades são decodificadas. Os seguintes sinalizadores podem ser definidos:
    
TNEF_PROP_EXCLUDE 
  
> Decodifica todas as propriedades não especificadas no parâmetro _lpPropList_ . 
    
TNEF_PROP_INCLUDE 
  
> Decodifica todas as propriedades especificadas em _lpPropList_.
    
 _lpPropList_
  
> no Um ponteiro para a lista de propriedades para incluir ou excluir da operação de decodificação.
    
 _lpProblems_
  
> bota Um ponteiro para um ponteiro para uma estrutura [STnefProblemArray](stnefproblemarray.md) retornada. A estrutura **STnefProblemArray** indica quais propriedades, se houver, não foram codificadas corretamente. Se NULL for passado no parâmetro _lpProblems_ , nenhuma matriz de problemas de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_CORRUPT_DATA 
  
> Os dados que estão sendo decodificados em um Stream estão corrompidos.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: ExtractProps** para extrair (ou seja, decodificar) Propriedades do encapsulamento de uma mensagem ou de um anexo que foi passado para a função [OpenTnefStream](opentnefstream.md) . O provedor de chamadas ou o gateway pode especificar uma lista de propriedades a serem decodificadas. Provedores e gateways também podem usar o **ExtractProps** para fornecer informações sobre o tratamento especial de anexos. 
  
 **ExtractProps** preenche a mensagem original passada para **OpenTnefStream** com as propriedades decodificadas. As chamadas **ExtractProps** subsequentes voltarão para a mensagem e extrairão a nova lista de propriedades. 
  
Ao contrário do método [ITnef::](itnef-addprops.md) addprops, que enfileira as ações solicitadas até que o método **ITnef:: Finish** seja chamado, o método **ExtractProps** decodifica as propriedades encapsuladas imediatamente quando ele é chamado. Por esse motivo, a mensagem de destino para decodificação de encapsulamento deve ser relativamente vazia. As propriedades existentes na mensagem de destino são sobrescritas por Propriedades encapsuladas. 
  
 **ExtractProps** só tem suporte para objetos abertos com o sinalizador TNEF_DECODE para a função **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) . 
  
A implementação TNEF relata os problemas de codificação de fluxo TNEF sem interromper o processo **ExtractProps** . A estrutura [STnefProblemArray](stnefproblemarray.md) retornada no _lpProblems_ indica quais atributos TNEF ou propriedades MAPI, se houver, não puderam ser processados. O valor retornado no membro **SCODE** de uma das estruturas **STnefProblem** contidas no **STnefProblemArray** indica o problema específico. O provedor ou gateway pode funcionar na pressuposição de que todas as propriedades ou atributos para os quais o **ExtractProps** não retorna um relatório de problemas foram processados com êxito. 
  
> [!NOTE]
> Se uma propriedade no bloco de encapsulamento MAPI não puder ser processada e deixar o fluxo não confiável durante a decodificação de um fluxo TNEF, a decodificação do bloco de encapsulamento será interrompida e um problema será relatado. A matriz problemática para esse tipo de problema contém 0L para o membro **ulPropTag** `attMAPIProps` `attAttachment` ou para o membro **ulAttribute** e MAPI_E_UNABLE_TO_COMPLETE para o membro **SCODE** . Observe que a decodificação do Stream não é interrompida, apenas a decodificação do bloco de encapsulamento MAPI. A decodificação de fluxo continua com o próximo bloco de atributos. 
  
Se um provedor ou gateway não funcionar com matrizes problemáticas, ele poderá passar NULL no _lppProblems_; Nesse caso, nenhum conjunto de problemas é retornado. 
  
O valor retornado em _lpProblems_ é válido somente se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na estrutura **STnefProblemArray** . Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamadas ou o gateway não deverá usar ou liberar a estrutura. Se nenhum erro ocorrer na chamada, o provedor de chamada ou o gateway deve liberar a memória para a estrutura **STnefProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

