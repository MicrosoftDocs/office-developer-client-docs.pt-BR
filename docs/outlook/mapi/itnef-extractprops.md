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
  
> [in] Uma bitmask de sinalizadores que controla como as propriedades são decodificadas. Os sinalizadores a seguir podem ser definidos:
    
TNEF_PROP_EXCLUDE 
  
> Decodifica todas as propriedades não especificadas no _parâmetro lpPropList._ 
    
TNEF_PROP_INCLUDE 
  
> Decodifica todas as propriedades especificadas em  _lpPropList_.
    
 _lpPropList_
  
> [in] Um ponteiro para a lista de propriedades a incluir ou excluir da operação de decodificação.
    
 _lpProblems_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura STnefProblemArray](stnefproblemarray.md) retornada. A **estrutura STnefProblemArray** indica quais propriedades, se alguma, não foram codificadas corretamente. Se NULL for passado no  _parâmetro lpProblems,_ nenhuma matriz de problema de propriedade será retornada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_CORRUPT_DATA 
  
> Os dados que estão sendo decodificados em um fluxo estão corrompidos.
    
## <a name="remarks"></a>Comentários

Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::ExtractProps** para extrair (ou seja, decodificar) propriedades do encapsulamento de uma mensagem ou um anexo que foi passado para a função [OpenTnefStream.](opentnefstream.md) O provedor de chamada ou gateway pode especificar uma lista de propriedades a decodificar. Provedores e gateways também podem usar **ExtractProps** para fornecer informações sobre qualquer tratamento especial para anexos. 
  
 **ExtractProps** preenche a mensagem original passada para **OpenTnefStream** com as propriedades decodificadas. As **chamadas ExtractProps subsequentes** voltarão à mensagem e extrairão a nova lista de propriedades. 
  
Ao contrário do método [ITnef::AddProps,](itnef-addprops.md) que enfileira ações solicitadas até que o método **ITnef::Finish** seja chamado, o método **ExtractProps** decodifica as propriedades encapsuladas imediatamente quando ele é chamado. Por esse motivo, a mensagem de destino para decodificação de encapsulamento deve estar relativamente vazia. As propriedades existentes na mensagem de destino são substituídas por propriedades encapsuladas. 
  
 **ExtractProps** é suportado apenas para objetos que são abertos com o sinalizador TNEF_DECODE para as funções **OpenTnefStream** ou [OpenTnefStreamEx.](opentnefstreamex.md) 
  
A implementação do TNEF relata problemas de codificação de fluxo TNEF sem interromper **o processo ExtractProps.** A [estrutura STnefProblemArray](stnefproblemarray.md) retornada em  _lpProblems_ indica quais atributos TNEF ou propriedades MAPI, se algum, não puderam ser processados. O valor retornado no membro **scode** de uma das estruturas **STnefProblem** contidas em **STnefProblemArray** indica o problema específico. O provedor ou gateway pode trabalhar na suposição de que todas as propriedades ou atributos para os quais **ExtractProps** não retorna um relatório de problemas foram processados com êxito. 
  
> [!NOTE]
> Se uma propriedade no bloco de encapsulamento MAPI não puder ser processada e deixar o fluxo não confiável durante a decodificação de um fluxo TNEF, a decodificação do bloco de encapsulamento será interrompida e um problema será relatado. A matriz do problema para esse tipo de problema contém 0L para o membro **ulPropTag** ou para o membro `attMAPIProps` `attAttachment` **ulAttribute** e MAPI_E_UNABLE_TO_COMPLETE para o membro **scode.** Observe que a decodificação do fluxo não é interrompida, apenas a decodificação do bloco de encapsulamento MAPI. A decodificação de fluxo continua com o próximo bloco de atributos. 
  
Se um provedor ou gateway não funcionar com matrizes de problemas, ele poderá passar NULL em  _lppProblems_; nesse caso, nenhuma matriz do problema será retornada. 
  
O valor retornado em  _lpProblems_ só será válido se a chamada retornar S_OK. Quando S_OK é retornado, o provedor ou gateway deve verificar os valores retornados na **estrutura STnefProblemArray.** Se ocorrer um erro na chamada, a estrutura **STnefProblemArray** não será preenchida e o provedor de chamada ou gateway não deverá usar ou liberar a estrutura. Se não ocorrer nenhum erro na chamada, o provedor de chamada ou gateway deverá liberar a memória para a estrutura **STnefProblemArray** chamando a função [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Confira também



[ITnef::AddProps](itnef-addprops.md)
  
[ITnef::Finish](itnef-finish.md)
  
[ITnef::SetProps](itnef-setprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)

